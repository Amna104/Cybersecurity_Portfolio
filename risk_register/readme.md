# Risk Register for a Banking Environment

## Overview
This project demonstrates the creation of a risk register for a small coastal bank. The bank has 100 on-premise employees and 20 remote employees, servicing 2,000 individual accounts and 200 commercial accounts. The activity evaluates potential risks to the bank’s assets and proposes prioritization for mitigation.

## Operational Environment
- Coastal area with low crime rates
- 100 on-premise and 20 remote employees
- Customer base: 2,000 individual accounts, 200 commercial accounts
- Financial regulations require secure handling of funds and data

## Risk Assessment Methodology
1. **Identify assets**: Funds, user data, financial records, physical assets, and supply chain dependencies.
2. **Identify risks**: Potential threats like business email compromise, theft, financial data leaks, and supply chain disruptions.
3. **Analyze risks**: Assign scores for likelihood (1-3) and severity (1-3) based on potential impact.
4. **Calculate priority**: Multiply likelihood by severity to determine which risks require immediate attention.

## Risk Register

| Asset | Risk(s) | Description | Likelihood | Severity | Priority |
|-------|---------|-------------|-----------|---------|---------|
| Funds | Business email compromise | An employee is tricked into sharing confidential information | 2 | 2 | 4 |
| Funds | Compromised user database | Customer data is poorly encrypted | 2 | 3 | 6 |
| Funds | Financial records leak | Database server of backed-up data is publicly accessible | 3 | 3 | 9 |
| Funds | Theft | The bank's safe is left unlocked | 1 | 3 | 3 |
| Funds | Supply chain disruption | Delivery delays due to natural disasters | 1 | 2 | 2 |

## Notes
- Partnerships with other companies can increase risk exposure.  
- Theft risk is less prioritized due to the low-crime environment.  
