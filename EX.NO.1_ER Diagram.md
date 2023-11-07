# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE:
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm

1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![er](https://github.com/DrUmaRaniV/DBMS/assets/118707332/e5bff67b-f0c1-4de2-bade-de09a6862ed7)


### Relational model

![relational](https://github.com/DrUmaRaniV/DBMS/assets/118707332/8985a513-d0d4-4163-8f61-0e71c5d091d7)

### SQL DDL Schema 
```
CREATE TABLE BANK
(
  CODE INT NOT NULL,
  NAME INT NOT NULL,
  ADDRESS INT NOT NULL,
  PRIMARY KEY (CODE)
);

CREATE TABLE BANK_BRANCH
(
  ADDRESS INT NOT NULL,
  BRANCH_NO INT NOT NULL,
  PRIMARY KEY (BRANCH_NO)
);

CREATE TABLE ACCOUNTS
(
  ACCT_NO INT NOT NULL,
  BALANCE INT NOT NULL,
  TYPE INT NOT NULL,
  PRIMARY KEY (ACCT_NO)
);

CREATE TABLE LOAN
(
  LOAN_NO INT NOT NULL,
  AMOUNT INT NOT NULL,
  TYPE INT NOT NULL,
  PRIMARY KEY (LOAN_NO)
);

CREATE TABLE CUSTOMER
(
  SSN INT NOT NULL,
  NAME INT NOT NULL,
  ADDRESS INT NOT NULL,
  PHONE INT NOT NULL,
  PRIMARY KEY (SSN)
);
```
## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
