\# Data Dictionary — FinPay Analytics Dashboard



This document describes every field used in the transformed fact and dimension tables.



---



\## FACT TABLE



\### \*\*fact\_transactions\*\*

| Column Name        | Description                                                                 |

|--------------------|-----------------------------------------------------------------------------|

| transaction\_id     | Unique identifier for each transaction                                      |

| user\_id            | Foreign key to dim\_user                                                     |

| merchant\_id        | Foreign key to dim\_merchant                                                 |

| amount             | Transaction amount in INR                                                   |

| currency           | Currency code (INR in this dataset)                                         |

| payment\_method     | Payment type used (UPI, Wallet, Card, etc.)                                 |

| status             | Status of the transaction (success, failed, refund)                         |

| transaction\_ts     | Timestamp of when the transaction occurred                                  |

| category           | Merchant category (shopping, food, bill payment, etc.)                      |

| country            | Country associated with the transaction                                     |

| device\_type        | Device used (Android, iOS, Web)                                             |

| is\_promo\_used      | Indicates if a promotion was used (Yes/No or Boolean)                       |

| YearMonth          | YYYYMM format for month-level calculations                                  |



---



\## DIMENSION TABLES



\### \*\*dim\_user\*\*

| Column Name      | Description                        |

|------------------|------------------------------------|

| user\_id          | Primary key                        |

| signup\_date      | User signup date (if generated)    |

| user\_country     | Country of the user                |

| user\_device      | Device type information (optional) |



---



\### \*\*dim\_merchant\*\*

| Column Name       | Description                                   |

|-------------------|-----------------------------------------------|

| merchant\_id       | Primary key                                   |

| merchant\_name     | Merchant name                                 |

| merchant\_category | Category (food, retail, travel, etc.)         |

| merchant\_country  | Country associated with the merchant          |



---



\### \*\*dim\_payment\_method\*\*

| Column Name          | Description                                 |

|----------------------|---------------------------------------------|

| payment\_method\_id    | Primary key                                 |

| payment\_method\_name  | Payment method label (UPI, Wallet, Card)    |

| payment\_type\_group   | Optional grouping (Online, Offline, Others) |



---



\### \*\*dim\_country\*\*

| Column Name | Description                       |

|-------------|-----------------------------------|

| country     | Country name or country code      |

| region      | Optional regional grouping         |



---



\### \*\*dim\_device\*\*

| Column Name  | Description                   |

|--------------|-------------------------------|

| device\_type  | Android / iOS / Web           |



---



\### \*\*dim\_date\*\*

| Column Name      | Description                               |

|------------------|-------------------------------------------|

| date             | Full date (YYYY-MM-DD)                    |

| year             | Year number                               |

| month            | Month number                              |

| month\_name       | Month name (Jan, Feb, etc.)               |

| year\_month       | YYYY-MM format                            |

| day              | Day number                                |

| day\_name         | Day name (Mon, Tue, etc.)                 |

| week\_number      | Week number                               |



---



\## Notes

\- All dimension tables connect to \*\*fact\_transactions\*\* using their primary keys.

\- This structure follows the \*\*Star Schema\*\* model optimized for BI reporting.



