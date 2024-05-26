<h1>Backend Architecture for Digital Banking Application</h1>
<h2>Digital Banking Application </h2>
    <h3>Overview</h3>
    <p>This digital banking application is designed to manage bank operations securely and efficiently. It features functionalities for both administrative and regular users, supported by a robust backend built with Spring, a dynamic and responsive frontend with Angular, and enhanced security through JWT.</p>

<h3>Functionalities</h3>
    <h3>Login Page</h3>
    <p>The login page allows users to enter their credentials. Based on their role (admin or user), they are directed to the appropriate dashboard with functionalities tailored to their permissions.</p>

<h3>Dashboard</h3>
    <p>The main dashboard is accessible post-login and provides links to various functionalities depending on the user's role.</p>

<h3>Customer Management</h3>
    <ul>
        <li><strong>Customer List:</strong> Displays all customers with options to edit, delete, or view detailed account information for each customer.</li>
        <li><strong>Add Customer:</strong> Allows the creation of new customer records.</li>
        <li><strong>Edit/Delete Customer:</strong> Admins can modify or remove existing customer details.</li>
    </ul>

<h3>Account Operations</h3>
    <ul>
        <li><strong>Perform Transaction:</strong> Allows the user to perform debit, credit, or transfer operations between accounts.</li>
        <li><strong>Account Details:</strong> Users can search for specific accounts to view transaction history and account balances.</li>
    </ul>

<h3>Security and Data Protection</h3>
    <p>The application uses Secure Real-time Transport Protocol (SRTP) to enhance the security of data transmission, ensuring that all user data and financial transactions are encrypted and secure against unauthorized access.</p>

<h3>Roles and Permissions</h3>
    <p>There are two primary roles in the application:</p>
    <ul>
        <li><strong>Admin:</strong> Can manage customers, perform transactions on behalf of customers, view all accounts, and access comprehensive administrative tools.</li>
        <li><strong>Normal User:</strong> Primarily focused on managing their own account, viewing transaction history, and performing personal account transactions.</li>
    </ul>
    
  <h2>Project Structure</h2>
    <h3>Data Transfer Objects (DTOs)</h3>
    <ul>
        <li><strong>AccountHistoryDTO, AccountOperationDTO, BankAccountDTO:</strong> These DTOs carry necessary data related to account transactions and operations between the server and clients.</li>
        <li><strong>CurrentBankAccountDTO, SavingBankAccountDTO:</strong> Specific DTOs for different types of bank accounts, supporting specialized operations for each.</li>
        <li><strong>CustomerDTO:</strong> Manages data transfer concerning customer information.</li>
    </ul>

   <h3>Entities and Enums</h3>
    <ul>
        <li><strong>AccountStatus, OperationType:</strong> Enums to define constant values for account statuses and operation types to ensure consistency across the application.</li>
        <li><strong>Entities like AccountOperation, BankAccount, Customer, etc.:</strong> These represent the application's core business logic and are mapped directly to the database schema.</li>
    </ul>

  <h3>Repositories</h3>
    <ul>
        <li><strong>AccountOperationRepository, BankAccountRepository, CustomerRepository:</strong> Interfaces for managing database interactions for account operations, bank accounts, and customer data, respectively.</li>
    </ul>

  <h3>Services</h3>
    <ul>
        <li><strong>BankAccountService, BankService:</strong> Core service components that handle business logic related to bank operations and transactions.</li>
    </ul>

   <h3>Security</h3>
    <ul>
        <li><strong>SecurityConfig:</strong> Configures security settings for the application, managing authentication and authorization.</li>
    </ul>

  <h3>Web Controllers</h3>
    <ul>
        <li><strong>BankAccountRestAPI, CustomerRestController:</strong> Controllers that expose RESTful APIs to handle requests related to bank accounts and customer management.</li>
    </ul>

  <h3>Configuration and Execution</h3>
    <ul>
        <li><strong>DigitalBankingBackendApplication:</strong> The main class that starts the Spring Boot application.</li>
        <li><strong>application.properties:</strong> Contains configuration settings for the application, such as database connection details and application-specific properties.</li>
    </ul>

  <h2>Conclusion</h2>
    <p>This structured approach using Spring ensures that the backend is robust, secure, and capable of handling complex business requirements and operations of a digital banking platform.</p>
