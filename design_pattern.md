Repository ????

    Vietnamese:
    
        Repository Pattern là lớp trung gian giữa tầng Data Access và Business Logic, hiểu môm na thì nó là lớp trung gian giữa việc truy cập dữ liệu và xử lý logic. giúp cho việc truy cập dữ liệu chặt chẽ và bảo mật hơn

    Eng:

        Repository pattern is a kind of container where data access logic is stored. It hides the details of data access logic from business logic. In other words, we allow business logic to access the data object without having knowledge of underlying data access architecture

        what are common set of operations that can be applied to these two data objects? In most situations we want to have the following operations:
            - Get all records
            - Get paginated set of records
            - Create a new record
            - Get record by it’s primary key
            - Get record by some other attribute
            - Update a record
            - Delete a record