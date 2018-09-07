# Loan-Level-Calculator

The class is created for calculating loan information. Given the notional, interest rate, terms and the period you wannt to check, the calculator can return monthlypmt, makePrincipalPayment, makeInterestPayment, notionalBalance.

#### LoanInfo: Initialized with loan notional and rate.

#### StandardTranche derived from parent class LoanInfo. This child class keeps track of all interest payments and all principal payments made to it, and at what time period, implements the following methods:

monthlypmt: return the monthly payment

makePrincipalPayment: record a principal payment for the current object time period.

makeInterestPayment: record an interest payment for the current object time period.

notionalBalance: return the amount of notional still owed to the tranche for the current time period (after any payments made).

#### Calculation theory:

periodic loan payment: pmt = rP/(1-(1+r)^(-N) = rP(1+r)^N/((1+r)^N - 1) 

remaing balance: bal = P(1+r)^n - pmt[((1+r)^n-1)/r]

where:

P = Principal

r = Monthly interest rate

N = Term of loan

n = Number of payments made

pmt = Monthly payment

bal = Balance of Loan
