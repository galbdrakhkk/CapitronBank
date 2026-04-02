USE cbank;

CREATE TABLE sales_rawdata(
sales_person VARCHAR(50),
`2015` varchar(50),
`2016` varchar(50),
`2017` varchar(50),
`2018` varchar(50)
);

SELECT * 
FROM sales_rawdata;

INSERT INTO sales_rawdata
VALUES
('John', 'Five', 'Six', 'Five', 'Four'),
('Suzie', 'One', 'Two', 'Three', 'Four'),
('Dafney', 'One', 'One', 'Two', 'Four');

SELECT * 
FROM sales_rawdata;

SELECT sales_person,
CASE `2015`
WHEN 'Five' THEN 5
WHEN 'One' THEN 1
END as `2015`,

CASE `2016`
WHEN 'Six' THEN 6
WHEN 'Two' THEN 2
WHEN 'One' THEN 1
END as `2016`,

CASE `2017`
WHEN 'Five' THEN 5
WHEN 'Three' THEN 3
WHEN 'Two' THEN 2
END as `2017`,

CASE `2018`
WHEN 'Four' THEN 4
END as `2018`
FROM sales_rawdata;
 
UPDATE sales_rawdata
SET 
    `2015` = CASE 
        WHEN `2015` = 'Five' THEN 5
        WHEN `2015` = 'One' THEN 1
        ELSE `2015`
    END,

    `2016` = CASE 
        WHEN `2016` = 'Six' THEN 6
        WHEN `2016` = 'Two' THEN 2
        WHEN `2016` = 'One' THEN 1
        ELSE `2016`
    END,

    `2017` = CASE 
        WHEN `2017` = 'Five' THEN 5
        WHEN `2017` = 'Three' THEN 3
        WHEN `2017` = 'Two' THEN 2
        ELSE `2017`
    END,

    `2018` = CASE 
        WHEN `2018` = 'Four' THEN 4
        ELSE `2018`
    END;
    
    
SELECT sales_person, 2015 AS year, `2015` AS units_sold FROM sales_rawdata
UNION ALL
SELECT sales_person, 2016, `2016` FROM sales_rawdata
UNION ALL
SELECT sales_person, 2017, `2017` FROM sales_rawdata
UNION ALL
SELECT sales_person, 2018, `2018` FROM sales_rawdata;

-- tableau  Dashboard section 

CREATE TABLE sales_final AS
SELECT sales_person, 2015 AS year, `2015` AS units_sold FROM sales_rawdata
UNION ALL
SELECT sales_person, 2016, `2016` FROM sales_rawdata
UNION ALL
SELECT sales_person, 2017, `2017` FROM sales_rawdata
UNION ALL
SELECT sales_person, 2018, `2018` FROM sales_rawdata;


