1. **What is a list in Python, and how is it used in DevOps?**
    - A list in Python is a collection of items that are ordered and changeable. In DevOps, lists can be used to manage and manipulate data, such as configurations, server names, and deployment targets.
    - For example, you can use a list to store a list of servers that need to be provisioned or configured.

2. **How do you create a list in Python, and can you provide an example related to DevOps?**
    - In Python, we can create a list using square brackets `[]`.
    - Example:
      ```python
      servers = ['server1', 'server2', 'server3']
      ```

3. **What is the difference between a list and a tuple in Python, and when would you choose one over the other in a DevOps context?**
    - The key difference is mutability; Lists are mutable, whereas tuples are immutable.
    - Use lists when you need to modify the collection (e.g., a list of active servers, configuration settings that may be updated), and tuples when the collection should remain constant (e.g., server configurations, deployment steps).

4. **How can you access elements in a list, and provide a DevOps-related example?**
    - Elements in a list can be accessed using their index.
    - Example: If we have a list of server names and want to access the first server, we would do the following:
      ```python
      servers = ['server1', 'server2', 'server3']
      print(servers[0])  # Output: server1
      ```

5. **How do you add an element to the end of a list in Python? Provide a DevOps example.**
    - We can add an element to the end of a list using the `append()` method.
    - Example: If we want to add a new server to a list of servers, we can do this
      ```python
      servers = ['server1', 'server2']
      servers.append('server3')
      ```

6. **How can you remove an element from a list in Python, and can you provide a DevOps use case?**
    - We can remove an element from a list using the `remove()` method.
    - Example: We might want to remove a server from a list of servers that are no longer needed
      ```python
      servers = ['server1', 'server2', 'server3']
      servers.remove('server2')
      ```

7. **Describe a real-world example of how you used Python to solve a DevOps challenge.**
    - I automate the Jira ticket creation using GitHub Webhook with Python:
      - In a GitHub repository, where the QA team or developers would raise issues whenever they found bugs in the code. After an issue was raised, a developer would review it and, if the issue was critical, create a JIRA ticket for organizational tracking and resolution. The process of manually creating JIRA tickets for every issue was time-consuming.
      - To automate this, I used Python to streamline the process. We created a GitHub webhook that would listen for comments on the issues in the repository. Whenever someone commented with the keyword /jira, it would trigger a Python script that automatically created a JIRA ticket. This saved time by eliminating the need to manually create tickets for each issue.
      - The reason we chose to use /jira in the comments as a trigger was to ensure that the issue was well-understood and clearly described before a ticket was created. This way, developers would not create JIRA tickets prematurely, avoiding unnecessary or incomplete tickets.
      - This automation significantly improved our workflow, ensuring that critical issues were tracked in JIRA without manual intervention, allowing developers to focus more on resolving the issues rather than managing ticket creation.

8. **Discuss the challenges that you faced while using Python for DevOps and how did you overcome it.**
    - When I was using Python for DevOps to automate JIRA ticket creation, I faced a couple of challenges. One of the main issues was figuring out the `issue type ID` and `leadAccountId`.
    - To overcome this, I referred to the official JIRA API documentation and also explored the JIRA UI to find the necessary values.
    - As my experience is that it's very important to understand the manual process before automating. Knowing how things work manually makes it much easier to define the required values and troubleshoot any issues during the automation process.

9. **How can you secure your Python code and scripts?**
    - I secure my Python code by handling sensitive information using input variables, command-line arguments, or environment variables instead of hardcoding them in the code.

10. **Explain the difference between mutable and immutable objects.**
     - Mutable objects can be changed after creation (e.g., lists), while immutable objects cannot be changed once created (e.g., tuples).

11. **Differentiate between list and tuple in Python.**
     - Lists are mutable, defined with `[]` and typically used for storing collections of items that can be changed, while tuples are immutable, defined with `()` and commonly used to store collections of items that shouldn't change.

12. **Explain the use of virtualenv.**
     - `virtualenv` is used to create isolated Python environments to manage dependencies for different projects. It allowing different projects to use different versions of packages without conflicts.
     - Example:
       - Creating a virtual environment named 'myenv' → `virtualenv myenv`
       - Activating the virtual environment:
         - On Windows → `myenv\Scripts\activate`
         - On Unix or MacOS → `source myenv/bin/activate`

13. **What are decorators in Python?**
     - Decorators modify the behavior of functions. They take a function as an argument, add some functionality, and return another function without modifying the original function's code.
     - Example:
        ```python
        def my_decorator(func):
            def wrapper():
                print("Something is happening before the function is called.")
                func()
                print("Something is happening after the function is called.")
            return wrapper

        @my_decorator
        def say_hello():
            print("Hello!")

        say_hello()
        ```
     - Output:
        ```
        Something is happening before the function is called.
        Hello!
        Something is happening after the function is called.
        ```

14. **How does exception handling work in Python?**
     - Python uses try-except blocks to handle exceptions and prevent program crashes.
     - Exception handling in Python uses `try`, `except`, `else` and `finally` blocks.
     - Example: Handling division by zero exception
        ```python
        try:
            result = 10 / 0
        except ZeroDivisionError:
            print("Division by zero is not allowed.")
        else:
            print("Division successful:", result)
        finally:
            print("This block always executes.")
        ```

15. **What's the difference between append() and extend() for lists?**
     - `append()` adds a single element to the end of a list, while `extend()` adds multiple elements by appending elements from an iterable.
     - Example:
       - Using append():
            ```python
            my_list = [1, 2, 3]
            my_list.append(4)
            print(my_list)  # Output: [1, 2, 3, 4]
            ```
       - Using extend():
            ```python
            my_list = [1, 2, 3]
            my_list.extend([4, 5])
            print(my_list)  # Output: [1, 2, 3, 4, 5]
            ```

16. **Explain the use of lambda functions in Python.**
     - A lambda function is an anonymous function (i.e., a function without a name) that is defined using the `lambda` keyword.
     - It is mainly used for short, simple operations where a full function definition is unnecessary.
     - Syntax: `lambda arguments: expression`
     - Example:
        ```python
        add = lambda x, y: x + y
        print(add(3, 5))  # Output: 8
        ```

17. **What are the different types of loops in Python?**
     - Python has **three types** of loops.
       - `for loop`: To iterate over sequences (lists, tuples, strings, etc.)
            ```python
            for i in range(5):
                print(i)
            ```
       - `while loop`: Runs as long as the condition is `True`
            ```python
            i = 0
            while i < 5:
                print(i)
                i += 1
            ```
       - `nested loop`: A loop inside another loop
            ```python
            for i in range(2):
                for j in range(3):
                    print(i, j)
            ```

18. **Explain the difference between == and is operators.**
     - `==`	Operator: Checks if values are equal
     - `is` Operator: Checks if memory addresses are the same
     - Example:
        ```python
        a = [1, 2, 3]
        b = [1, 2, 3]
        c = a

        print(a == b)  # ✅ True (values are same)
        print(a is b)  # ❌ False (different memory locations)
        print(a is c)  # ✅ True (same memory location)
        ```

19. **What is the use of the pass keyword?**
     - The `pass` keyword is a **placeholder** that allows code to run without errors when a statement is required but no action is needed.
     - Use Cases:
       - When defining an `empty function` or `class`.
       - When writing code that will be implemented later.
     - Example:
        ```python
        def my_function():
            pass  # Function is empty but avoids an error

        class MyClass:
            pass  # Placeholder for future implementation

        for i in range(5):
            if i == 2:
                pass  # Placeholder for future logic
            else:
                print(i)
        ```

20. **What is the difference between global and local variables?**
     - Global variables are defined outside functions and can be accessed anywhere in the code, while local variables are defined inside functions and are only accessible within that function's scope.
     - Example:
        ```python
        x = 10  # Global variable

        def my_function():
            y = 5  # Local variable
            print(y)  # Accessible here

        my_function()
        print(x)  # Accessible outside

        # print(y)  # ❌ Error: y is local to my_function()
        ```

21. **Explain the difference between open() and with open() statement.**
     - `open()`: Opens a file, but requires manual closing using `close()`
     - `with open()`: Uses a context manager to open a file, automatically closing it after use
     - Example using `open()`:
        ```python
        file = open("test.txt", "r")
        content = file.read()
        print(content)
        file.close()  # Must manually close the file
        ```
     - Example using `with open()`:
        ```python
        with open("test.txt", "r") as file:
            content = file.read()
            print(content)
        # No need to manually close the file
        ```

22. **How can you use Python to interact with AWS services? Provide an example.**
     - Python interacts with AWS services using the **Boto3** library.
     - Example: Listing S3 Buckets
        ```python
        import boto3

        s3 = boto3.client('s3')
        buckets = s3.list_buckets()

        for bucket in buckets['Buckets']:
            print(bucket['Name'])
        ```

23. **What is Boto3, and how is it used in AWS automation with Python?**
     - Boto3 is the **Official AWS SDK for Python** that allows developers to interact with AWS services programmatically.
     - Boto3 is used in AWS Automation:
       - Managing EC2 instances (start, stop, terminate)
       - Uploading and downloading files to S3
       - Automating infrastructure provisioning (creating VPCs, subnets)
       - Working with AWS Lambda, DynamoDB, SNS, SQS, etc.

24. **How can you manage AWS EC2 instances using Python scripts?**
     - We can use **Boto3** to manage EC2 instances programmatically.
     - Example: Starting and Stopping EC2 Instances
        ```python
        import boto3

        ec2 = boto3.client('ec2')

        instance_ids = ["i-0abcdef1234567890", "i-0abcdef1234567891"]  # Replace with your instance IDs

        # Start instances
        ec2.start_instances(InstanceIds=instance_ids)
        print(f"Starting EC2 instances: {instance_ids}")

        # Stop instances
        ec2.stop_instances(InstanceIds=instance_ids)
        print(f"Stopping EC2 instances: {instance_ids}")
        ```

25. **Explain how to use Python for AWS Lambda functions.**
     - AWS Lambda lets you run code without managing servers. Python can be used to write and deploy Lambda functions.
     - **Steps to create a Python-based Lambda function:**
       - Write a Python script
            ```python
            def lambda_handler(event, context):
                return {
                    "statusCode": 200,
                    "body": "Hello from AWS Lambda!"
                }
            ```
       - Upload the script to AWS Lambda (via AWS Console, AWS CLI, or Boto3).
       - Configure a trigger (API Gateway, S3, DynamoDB, etc.).
       - Execute the function when the trigger occurs.

26. **How can you automate AWS S3 bucket operations using Python?**
     - We can automate AWS S3 operations using **Boto3**, the AWS SDK for Python.
     - Common Automated S3 Operations:
       - Create a new S3 bucket
       - Upload/download files
       - List objects in a bucket
       - Delete objects or buckets
     - Example: Automating S3 Bucket Operations
        ```python
        import boto3

        s3 = boto3.client('s3')

        bucket_name = "my-unique-bucket-name"

        # Create a new bucket
        s3.create_bucket(Bucket=bucket_name)
        print(f"Bucket '{bucket_name}' created successfully.")

        # Upload a file
        s3.upload_file("local_file.txt", bucket_name, "uploaded_file.txt")
        print("File uploaded successfully!")

        # List objects in the bucket
        response = s3.list_objects_v2(Bucket=bucket_name)
        for obj in response.get('Contents', []):
            print(obj['Key'])

        # Delete a file
        s3.delete_object(Bucket=bucket_name, Key="uploaded_file.txt")
        print("File deleted successfully!")

        # Delete the bucket
        s3.delete_bucket(Bucket=bucket_name)
        print("Bucket deleted successfully!")
        ```

27. **Describe a scenario where you used Python to optimize AWS costs.**
     - One way Python can optimize AWS costs is by automating the management of idle resources, particularly EC2 instances. In a real-world scenario, I wrote a Python script using Boto3 to identify EC2 instances that were running but not being actively used. The script would stop instances after a certain period of inactivity to reduce compute costs.

28. **How does Python help in AWS DevOps automation?**
     - Python plays a key role in **AWS DevOps Automation** by integrating with AWS services through **Boto3**, enabling the automation of infrastructure, deployment, monitoring, and Cost Management.

29. **Explain the difference between lists, tuples, and dictionaries in Python.**
     - Lists are ordered and mutable, meaning their contents can be changed, and they allow duplicates.
     - Tuples are ordered and immutable, meaning their contents cannot be changed, but they allow duplicates.
     - Dictionaries are unordered but mutable key-value pairs, meaning their values can be changed, but the keys must be unique and they do not guarantee order (although they maintain insertion order since Python 3.6+).
     - Example:
          ```python
          my_list = [1, 2, 3]  # Mutable, allows duplicates
          my_tuple = (1, 2, 3)  # Immutable, allows duplicates
          my_dict = {"name": "Alice", "age": 25}  # Key-value pairs
          ```

30. **What are `*args` and `**kwargs` in Python functions?**  
     - `*args` and `**kwargs` allow functions to accept a variable number of arguments.
     - **`*args` (Non-Keyword Arguments)**
       - Allows you to pass **multiple positional arguments** to a function.
       - Inside the function, `*args` is treated as a tuple.
       - **Example:**  
          ```python
          def add_numbers(*args):
              return sum(args)

          print(add_numbers(1, 2, 3, 4))  # Output: 10
          ```
     - **`**kwargs` (Keyword Arguments)**
       - Allows you to pass **multiple keyword arguments** (key-value pairs).
       - Inside the function, `**kwargs` is treated as a dictionary.
       - **Example:**  
          ```python
          def person_details(**kwargs):
              for key, value in kwargs.items():
                  print(f"{key}: {value}")

          person_details(name="Alice", age=25, city="New York")
          ```
       - **Output:**  
          ```
          name: Alice
          age: 25
          city: New York
          ```
     - **Using `*args` and `**kwargs` Together**
          ```python
          def sample_function(a, b, *args, **kwargs):
              print(f"a: {a}, b: {b}")
              print("Args:", args)
              print("Kwargs:", kwargs)

          sample_function(1, 2, 3, 4, name="Alice", age=25)
          ```
       - **Output:**
          ```
          a: 1, b: 2
          Args: (3, 4)
          Kwargs: {'name': 'Alice', 'age': 25}
          ```

31. **How would you use Python and Boto3 to list all EC2 instances in a region?**
     - Boto3 is the AWS SDK for Python that allows you to interact with AWS services like EC2.
     - Example:
        ```python
        import boto3

        ec2 = boto3.client('ec2')

        response = ec2.describe_instances()
        
        for reservation in response['Reservations']:
             for instance in reservation['Instances']:
                  print(instance['InstanceId'])
        ```
     - **Explanation:**
       - `boto3.client('ec2', region_name='us-east-1')` → Creates an EC2 client for the specified region.
       - `describe_instances()` → Fetches all EC2 instances.
       - Loops through `response['Reservations']` to extract and print instance details.