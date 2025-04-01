## 1. What is PostgreSQL?
### Ans : 
PostgreSQL হলো একটি ওপেন-সোর্স অবজেক্ট-রিলেশনাল ডাটাবেস ম্যানেজমেন্ট সিস্টেম, যা স্কেলেবিলিটি ও স্থিতিশীলতার জন্য পরিচিত।

## 2. What is the purpose of a database schema in PostgreSQL? 
### Ans  : 
একটি ডাটাবেস স্কিমা হলো একটি ফোল্ডারের মতো যা বিভিন্ন ডাটাবেস অবজেক্ট সংগঠিত করে। এটি ডাটাগুলো সাজিয়ে রাখে, নাম সম্পর্কিত সমস্যা এড়াতে সাহায্য করে এবং নির্দিষ্ট অংশগুলোর অ্যাক্সেস নিয়ন্ত্রণ করতে দেয়।

## 3. Explain the Primary Key and Foreign Key concepts in PostgreSQL. 
### Ans  : 
Primary Key: প্রতিটি রেকর্ডকে ইউনিকভাবে শনাক্ত করে। </br>
Foreign Key: একটি টেবিলের সাথে অন্য একটি টেবিলের সম্পর্ক তৈরি করে প্রাইমারি কী রেফারেন্সের মাধ্যমে।

## 4.What is the difference between the VARCHAR and CHAR data types? 
### Ans : 
VARCHAR: পরিবর্তনশীল দৈর্ঘ্যের স্ট্রিং সংরক্ষণ করে।</br>
CHAR: নির্দিষ্ট দৈর্ঘ্যের স্ট্রিং সংরক্ষণ করে এবং খালি স্থান দ্বারা পূরণ করে।

## 5. Explain the purpose of the WHERE clause in a SELECT statement. 
### Ans  : 
 WHERE ক্লজ নির্দিষ্ট শর্ত অনুসারে সারিগুলো ফিল্টার করতে ব্যবহৃত হয়।

## 6. What are the LIMIT and OFFSET clauses used for? 
### Ans  : 
LIMIT: রিটার্ন হওয়া সারির সংখ্যা সীমিত করে।</br>
OFFSET:  নির্দিষ্ট সংখ্যক সারি বাদ দিয়ে পরবর্তী সারি থেকে ডাটা দেখায়।

## 7. How can you modify data using UPDATE statements? 
### Ans  :  
UPDATE স্টেটমেন্ট নির্দিষ্ট শর্ত অনুযায়ী টেবিলের বিদ্যমান ডাটা পরিবর্তন করতে ব্যবহৃত হয়।
```
UPDATE customers
SET name = 'Alice'
WHERE id = 1; 

```

## 8. What is the significance of the JOIN operation, and how does it work in PostgreSQL? 
### Ans : 
JOIN অপারেশন দুটি বা ততোধিক টেবিলের সারি (rows) একত্রে আনতে ব্যবহৃত হয়, যেখানে সম্পর্কিত কলাম থাকে।
```
SELECT * FROM customers
 JOIN orders ON customers.id = orders.customer_id; 
```

## 9. Explain the GROUP BY clause and its role in aggregation operations. 
### Ans  :
 GROUP BY ক্লজ নির্দিষ্ট কলামের মান অনুসারে সারিগুলো গ্রুপ করে এবং অ্যাগ্রিগেট ফাংশন (COUNT(), SUM(), ইত্যাদি) প্রয়োগ করতে সাহায্য করে।

```
SELECT customer_id, COUNT(*) FROM orders
GROUP BY customer_id;

```
## 10. How can you calculate aggregate functions like COUNT(), SUM(), and AVG() in PostgreSQL? 
### Ans :
1. COUNT(): নির্দিষ্ট সেটের সারির সংখ্যা গণনা করে। </br>
   ```
   SELECT COUNT(*) FROM orders;

   ```
2. SUM(): একটি সংখ্যাসূচক কলামের মোট যোগফল গণনা করে।</br>
   ```
   SELECT SUM(order_amount) FROM orders;

   ```
3. AVG(): একটি সংখ্যাসূচক কলামের গড় মান নির্ণয় করে।</br>
   ```
   SELECT AVG(order_amount) FROM orders;

   ```

   