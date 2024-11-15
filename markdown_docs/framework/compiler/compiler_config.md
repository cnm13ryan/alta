## ClassDef Config
```python
class DatabaseManager:
    """
    A class designed to manage database operations such as connecting to a database,
    executing queries, and handling transactions.

    Attributes:
        connection (Connection): The database connection object.
        cursor (Cursor): The cursor object used for executing SQL commands.
    """

    def __init__(self, db_config):
        """
        Initializes the DatabaseManager with a configuration dictionary that contains
        necessary information to establish a database connection.

        Args:
            db_config (dict): A dictionary containing keys like 'host', 'user', 'password',
                             and 'database' which are used to connect to the database.
        """
        self.connection = None
        self.cursor = None
        self.connect(db_config)

    def connect(self, db_config):
        """
        Establishes a connection to the database using the provided configuration.

        Args:
            db_config (dict): The database configuration dictionary.
        """
        import mysql.connector
        try:
            self.connection = mysql.connector.connect(**db_config)
            self.cursor = self.connection.cursor()
        except Exception as e:
            print(f"Failed to connect to the database: {e}")

    def execute_query(self, query, params=None):
        """
        Executes a given SQL query with optional parameters.

        Args:
            query (str): The SQL query to be executed.
            params (tuple, optional): A tuple containing parameters for parameterized queries.

        Returns:
            list: A list of tuples representing the rows returned by the query.
        """
        try:
            if params:
                self.cursor.execute(query, params)
            else:
                self.cursor.execute(query)
            return self.cursor.fetchall()
        except Exception as e:
            print(f"Failed to execute query: {e}")
            return []

    def commit_transaction(self):
        """
        Commits the current transaction to make all changes permanent.
        """
        try:
            self.connection.commit()
        except Exception as e:
            print(f"Transaction failed to commit: {e}")

    def rollback_transaction(self):
        """
        Rolls back the current transaction, discarding any uncommitted changes.
        """
        try:
            self.connection.rollback()
        except Exception as e:
            print(f"Failed to roll back transaction: {e}")

    def close_connection(self):
        """
        Closes the database connection and cursor.
        """
        if self.cursor:
            self.cursor.close()
        if self.connection:
            self.connection.close()
```

This class, `DatabaseManager`, is designed to handle various aspects of database management including connecting to a database, executing SQL queries, managing transactions, and closing connections. It provides methods for each operation with clear documentation on their usage and expected parameters.
