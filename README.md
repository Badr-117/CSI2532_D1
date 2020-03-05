# CSI2532_Devoir#1
## Part A [60 points]: E-R Models
## A1 [15 points]: Relations, Cardinality and Participation
a)
![image](https://user-images.githubusercontent.com/44711173/75942778-4e7ee880-5e61-11ea-9154-a3ee65fb3c09.png)

b)
![image](https://user-images.githubusercontent.com/44711173/75942867-8554fe80-5e61-11ea-9b6e-7820f89f1af6.png)

c)
![image](https://user-images.githubusercontent.com/44711173/75942873-88e88580-5e61-11ea-823f-2ac48d933271.png)

## A2 [30 points]: System Design
![image](https://user-images.githubusercontent.com/44711173/75942915-a584bd80-5e61-11ea-91b6-a666be9ebea7.png)

## A3 [15 points]: Relational Algebra

![image](https://user-images.githubusercontent.com/44711173/75942931-b46b7000-5e61-11ea-818a-a61ed876df18.png)

## Part B [60 points]: SQL
## B1. [15 points] Reading SQL Queries
a)
![image](https://user-images.githubusercontent.com/44711173/75942985-d533c580-5e61-11ea-89c2-c0ce9c4a0783.png)

b)
![image](https://user-images.githubusercontent.com/44711173/75942991-d95fe300-5e61-11ea-98bb-66fe100e6170.png)

c)
![image](https://user-images.githubusercontent.com/44711173/75943007-e086f100-5e61-11ea-9098-9cac615e0316.png)
(Apres correction)
![image](https://user-images.githubusercontent.com/44711173/75943058-04e2cd80-5e62-11ea-9bcf-923674c5cc1c.png)

## B2. [15 points] Writing SQL Queries
a)
```
SELECT name FROM users WHERE join_date < '2020-01-01'
```

b)
```
SELECT COUNT(software_name), name FROM licenses 
JOIN users ON users.id = user_id
GROUP BY name
ORDER BY count DESC
```

c)
```
INSERT INTO licenses (user_id, software_name, access_code)
VALUES
 (50, 'Nord VPN', 'abc127'),
 (49, 'Android studio', 'def459'),
 (50, 'Eclips', 'hij779')
```

d)
```
UPDATE softwares
SET version = '51'
WHERE name = 'Sketch';
```
## B3. [30 marks] Updating SQL Schemas
a)
```
a)	ALTER TABLE licenses
ADD software_version varchar(100);

```

b)
```
ALTER TABLE softwares
DROP CONSTRAINT softwares_pkey;

ALTER TABLE softwares
ADD CONSTRAINT PK_softwares PRIMARY KEY (name,version);

```

c)
```
ALTER TABLE licenses
DROP CONSTRAINT licenses_pkey;

ALTER TABLE licenses
ADD CONSTRAINT PK_licenses PRIMARY KEY (user_id,software_name,software_version);

```

d)
```
UPDATE licenses
SET access_code = '1monthfree'
WHERE software_name = 'Sketch' AND software_version != '52'

```
