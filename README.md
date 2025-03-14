# 🏡 House Loan Calculation - Actuarial Mathematics

This Jupyter Notebook provides an **interactive frontend** for users and administrators to simulate house loan contract calculations based on **actuarial mathematics**. It leverages **Mercury** to create a user-friendly interface for both **end-users** and **administrators** to perform loan simulations and risk assessments.

---

## 🚀 Features
- **User Mode**: Input details like loan amount, interest rate, and maturity period to calculate monthly payments.
- **Admin Mode**: Simulate multiple random contracts for risk evaluation.
- **Actuarial Calculations**: Uses mortality tables and annuity factors to assess financial risks.
- **Supports Multiple Currencies**: EUR, USD, GBP.
- **Detailed Output**: Monthly payments, total interest, amortization schedule, and actuarial risk factors.

---

## 🛠️ Installation & Requirements

### 📌 Prerequisites
Ensure you have **Python 3.12+** and **Jupyter Notebook** installed.

Install all required dependencies located at _requirements.txt_ or use the following command:

```bash
pip install -r requirements.txt
```

### 🔧 Running the Notebook in the Browser
```bash
mercury run
```

You can access the Mercury frontend locally on [127.0.0.1](127.0.0.1)

## 📥 User Inputs
| Input                     | Description                          | Range                         |
|---------------------------|--------------------------------------|-------------------------------|
| Age (Years)               | Borrower's age                       | 18 -                      |
| Loan Amount               | Principal loan amount                | 0 -             |
| Yearly Interest Rate (%)  | Annual interest rate                 | 0.0 - 100.0                   |
| Maturity (Years)          | Loan term in years                   | 1 - 50                        |
| Mortality Table           | Select from TD88-90 or TH00-02 (France) |                       |
| Currency                  | Choose between EUR, USD, GBP         |                         |
| Admin Mode (Optional)     | Number of Random Contracts           | 1 - 1000                      |

## 📤 Output & Results
### Monthly Payment Calculation:
- Total loan repayment amount
- Monthly installment breakdown
- Interest and amortization schedule

### Actuarial Results:
- Single Premium: Present value of risk-adjusted benefits.
- Annual Premium: Yearly cost to cover loan risk.
- Monthly Premium: Monthly insurance-based risk cost.
- Annuity Factors: Adjusted for mortality rates and interest.

## 🔢 **Mathematical Formulas**

1. **Annuity Factor Calculation**  
𝑎ₓ(𝑚,𝑟) = ∑ᵢ₌₀ᴹ 𝑃(𝑥,𝑖,𝑟)

2. **Probability of Survival**  
   𝑃(𝑥,𝑛) = 𝑙ₓ₊ₙ / 𝑙ₓ

3. **Discount Factor**  
   𝐷𝐹(𝑛,𝑟) = 1 / (1 + 𝑟)ⁿ

4. **Loan Repayment Formula**  
   𝐴 = 𝑃⋅𝑟 / (1 - (1 + 𝑟)⁻ⁿ)

Where:
- 𝑥 = age of borrower.  
- 𝑚 = maturity in years.  
- 𝑟 = annual interest rate.  
- 𝑙ₓ = number of survivors from the mortality table at age 𝑥.  
- 𝑃 = loan amount.  
- 𝑁 = number of payments.

## 📄 License
This project is open-source under the MIT License.