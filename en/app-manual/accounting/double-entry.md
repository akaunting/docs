Double-Entry
============

Akaunting ships with a single-entry accounting feature set as it's easier to understand for most users. However, some businesses use double-entry accounting to keep their books.

Double-Entry accounting is a practice that helps minimize errors and increases the chance that your books balance. If you're an accountant, thanks to the multi-company feature of Akaunting, you can manage the financials of unlimited companies using this app.

Double-Entry app contains the following features:

- Chart of Accounts
- Manual Journal
- General Ledger
- Balance Sheet
- Trial Balance
- Opening/Starting Balance

## Dashboard

The dashboard is the landing page of the Akaunting, you can reach the Double-entry Dashboard below the Dashboard in the left side menu. The Double-Entry Dashboard gives you insight into the business activities of your company based on the COA. You can adjust the Double-Entry dashboard according to your needs. The dashboard shows you active fiscal year data of your company's financial activities by default; if you need, you can change the date range.

Following data display on the dashboard by default.
Widgets: Total Income by COA, Total Expense by COA, Total Profil by COA
Line Chart: Cash Flow
Pie Chart: Income by COA, Expense by COA
List: Account Balance, Latest Income By COA, Latest Expenses By COA

## Chart of Accounts

Double-Entry presents you a Chart of Accounts list that shows account types and its' details. You can see account types, what items they contain, types, and ability situations on this page and edit them. Chart of Account list page displays account code, account name, account, balance, and status. You can easily adjust the Chart of Account according to your needs.

You can add a new account, import your account list, or export yours in Akaunting from the button on the top right. To add a new account, just click the "Add New" button on the top right. If necessary, you can delete the default COA list and create or import your own COA list. Note that deleting and disabling are not possible if an account has associated with a transaction. You can view each account balance on this page. Additionally, each account's activities are listed by clicking related account. You can manage your transactions default account type on the Settings page.

In Double-Entry, all classes are collected under these 5 account types.

- Assets
- Liabilities
- Expenses
- Income
- Equity

### Creating a New Account

You can add a new account easily on the Chart of Accounts page. To do this, click on Add New button on the top right and fill in the required fields. After entering the account name, account type, code, and description (optional), you can save it by selecting whether it is enabled or disabled. If necessary, you can add a sub-account by entering the parent account.

![double-entry chart of accounts add new account](_images/DECOAAdd-New-Account.gif)

### Import and Export

You can export your COA list with one click at the right top of the COA page. To import your COA, you can find the import template on the import page, and then you can fill this excel table according to your request. You need to fill in the all required fields to complete the import. An account code can be added only for one account, if there is a duplicate account code on the import table, import is not completed. You can not add a new account type by importing a new COA list, you must use the previously added one. You can find the list of account Types below.
If you want to import the Revenues/Payments with a chart of accounts, you have to fill a column named chart_of_account that contains the code/name/id of an account.

Assets

- Bank & Cash
- Current Asset
- Depreciation
- Fixed Asset
- Inventory
- Non-current Asset
- Prepayment

Liabilities

- Current Liability
- Liability
- Non-current Liability
- Tax

Expenses

- Direct Costs
- Expense

Income

- Other Income
- Revenue
- Sales

Equity

- Equity

## Manual Journals

A manual journal is used to record any monetary movement of a business. Manual Journal is used to divided debit or credit into more than one account. Your transactions such as Sales, Purchase, Banking, etc are listed on the Double Entry reports. However, if you still need to create an additional entry, you can create a Manual Journal. If you create a manual journal for a transaction be aware that it may be duplicated data in reports.

There are some important steps when creating a manual journal:

- The date of the entry should be entered
- A description should be entered
- Every manual journal entry should be balanced. It means that the debits and credits have to total to the same amount. Otherwise, it cannot be saved until the credits and debits are matched.

![manual journals add new](_images/DEMJAdd-New1.gif)

## Reports

All reports of Double-Entry are available under the Reports pages, accessible from the left menu of Akaunting.

### General Ledger

A general ledger shows all movements of the chart of accounts that gives you insight into your company's financial health. All transactions details are listed on the General Ledger Report that includes your company's financial data used to create the firm's financial statements. It can be printed, exported, shared easily with one click on the General Ledger page. You can filter the General Ledger report by date, basis (cash accrual), contact, and COA.

![double-entry general ledger report](_images/DEReportsGL.gif)

### Balance Sheet

Balance Sheet shows the currents assets, receivables, debts, and capital of a business. Balance Sheet report can be found under the Reports from the menu. It can be printed, exported, shared easily with one click on the Balance Sheet page. You can filter the General Ledger report by date, basis (cash accrual).

![double-entry balance sheet report](_images/DEReportsBS.gif)

### Trial Balance

Trial Balance is a bookkeeping worksheet that shows whether debits and credits are equal or not. It can be printed, exported, shared easily with one click on the Trial Balance. You can filter the Trial Balance report by date, basis (cash accrual), and COA.

![double-entry trial balance report](_images/DEReportsTB.gif)

### Journals Entries

Journals Entries report shows all transactions that show a company's debit and credit balances. It can be printed, exported, shared easily with one click on the Journals Report page. You can filter the General Ledger report by date, basis (cash accrual), contact, and COA.

![double-entry journal entries report](_images/DEReportsJE.gif)

## Settings

### Default Chart of Accounts

You can manage your transactions default account type on the Settings page. Default Chart of Accounts makes it easier to keep your Double Entry ledgers.

- Invoice: Accounts Receivable records as Sales, if there is no account type on the related item.
- Bill: Accounts Payable records as General Expense, if there is no account type on the related item.
- Revenue records as Sales.
- Payment record as General Expense.
- If an invoice includes a discount, the discount amount records Sales Discount.
- If a bill includes a discount, the discount amount records Purchase Discount.

### Default Types

You can change default Bank & Cash and Tax types on the Settings page.

## FAQ

### How to enter the Opening/Starting Balance?

An opening balance is the amount of funds in an account at the beginning of a new fiscal period.

To set the opening balance, create a new entry from **Double-Entry > Journal Entry** page. Select the account for which you're setting the opening balance as first and the **Owner Contribution/Equity** (or an appropriate Equity) account as the second. Then:

1. If the opening balance account (first) is an **asset** (i.e. accounts receivable, bank, credit card), enter the amount as a **debit**.
2. If the opening balance account (first) is a **liability** (i.e. accounts payable), enter the amount as a **credit**.

![double-entry journal entries opening balance](_images/DEMJOpening-Balance.gif)

### How to customize the types or classes of the chart of accounts?

You can easily customize your Chart of Account list by adding new accounts or deleting accounts. If you have already using a Chart of Account, you can import it.

### What are the differences between Bookkeeping (Single-Entry) and Double-Entry?

The main difference is the number of the entires. Single entry has one cash-based entry for a transaction, in contrast, double-entry has 2 ledgers for a transaction as debit and credit.

### Why should I use the Double-Entry app?

Single entry is a quite simple accounting method for small businesses, that helps you to keep track of your company's income and expense statements. However, Double-Entry allows you to get detailed insight into your company's financial health. Double-entry accounting helps you to minimize errors and increases the chance that your books balance. You need to Double-Entry to generate Balance Sheet, General Ledger, Trial Balance reports. Additionally, Double Entry tracks your company's asset, equity, and liability balance.

## Terminology

### Assets

Assets are valuable things that belong to your business. Assets can contain things like office equipment, properties, or Accounts Receivable that your customer owes to your business for the service or product you provide and etc.

### Liabilities

Liabilities show your business's debts to other parties. It contains things like employee benefits payable, bank payments, tax payments and etc.

### Expenses

Expenses for goods and services used by your business are found in this section. You can find general expenses, legal expenses, rent expenses and etc. in this section, which is very useful for tracking operation costs, or you can tailor it to your needs as in other categories.

### Income

The revenue that your business earns is shown here. It includes items such as revenues from sales and investments etc.

### Equity

Equity shows the net worth of your business by representing the difference between your assets and liabilities. It contains things like owner contribution or owners draw etc.
