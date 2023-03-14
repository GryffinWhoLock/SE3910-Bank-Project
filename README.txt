# SE3910-Bank-Project
bookfrontend (react frontend): 
  components:
    BankUser: data model for bank user
    BookItem: data model for book (leftover from demo project)
    ExpenseIncome: data model for expenses and incomes (returns data model as table row)
    Header: header component (leftover from demo needs to be updated to be used for bank)
  pages:
    book:
      Detail: shows book with ability to delete or update (leftover from demo)
      Home: test attemptimg to receive information from the bank database (remove)
    user
      BalanceAdjustmentView: Balance adjust page with expense/income table and fields to create a new expense/income
      Detail: shows book with ability to delete or update (leftover from demo)
      JoinForm: Empty component (remove)
      LoginForm: Login page that calls the controller with username and password and redirecs to balance adjustment page if valid login
      SaveForm: Component to save book to repository (leftover from demo)
      UpdateForm: Component to update book in repository (leftover from demo)
  App.css: Contains css formatting that stores styles for components in app
  App.js: Contains main App and all routing to components
 
SpringReact (java backend):
  controller:
    BookController: (leftover from demo)
    ExpenseIncomeController: contains routes to backend service that use methods to query the expenses table in the database
    LoginController: Checks if username password combonination is valid by checking with the user table in the database (also contains leftover code)
    UserController: (leftover from demo)
    UserNotFoundException: (leftover from demo)
  domain:
    Account: (leftover)
    BankUser: bank user data model used to help send/receive information with react
    Book: (leftover)
    BookRepository: (leftover)
    ExpenseIncome: expense income data model usedd to help send/receive information with react
    Login: (leftover)
    Token: (leftover)
    User: (leftover)
  repository:
    AccountRepository: (leftover not using repositories using sql database)
    UserRepository: (leftover not using repositories using sql database)
  service:
    BookService: (leftover)
    SecurityServices: (leftover)
    UserService: (leftover)
  SpringReactApplication: launches backend server
  
bank.sql (creates database tables)
  tables:
    users:
      username varchar
      name varchar
      password varchar
      total_balance double
      savings_goal double
    expenses:
      username varchar foreign key
      expense_id char(5)
      planned int
      amount double
      income_or_expense int
      information varchar
      due_date date
