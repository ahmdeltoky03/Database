# `Relational Algebra and Calculus`

## **Chapter Outline**
- **Relational Algebra**
   - Unary Relational Operations 
   - Relational Algebra Operations From Set Theory
   - Binary Relational Operations
   - Additional Relational Operations
   - Examples of Queries in Relational Algebra
   
- **Relational Calculus**
   - Tuple Relational Calculus
   - Domain Relational Calculus
  
- **Example Database Application (COMPANY)**
- **Overview of the QBE language (appendix D)**


`Relational Algebra Overview`

- Relational algebra is the basic set of operations for the relational model .
- These operations enable a user to specify basic retrieval requests (or queries).
- The result of an operation is a new relation, which may have been formed from one or more input relations.

![](images\RRDS.png)

      ال Relational Algebra هي مجموعة العمليات التي يتم تنفيذها علي Relation معينة . يعني في الشكل الموضح عندي Relational Database schema خاصة بشركة معينة وال schema دي فيها اكتر من Relation فنا بنفذ بعض ال Relational Algebra علي ال Relation دي بحيث استرجع داتا معينة Retrieval Requests والداتا دي بترجع في صورة Relation ويمكن استخدام ال Relation دي في اكتر من عملية والعملية دي تسمي relational algebra expression .
     .A sequence of relational algebra operations forms a relational algebra expression

## **Relational Algebra consists of several groups of operations :**
* Unary Relational Operations
     - SELECT (sigma)
     - PROJECT (pi)
         

             مفهوم ال Unary Operator  انه بيتم تنفيذه علي Operation واحدة فقط .
      
* Relational Algebra Operations From Set Theory
     - UNION , INTERSECTION , DIFFERENCE (or MINUS, – )
     - CARTESIAN PRODUCT ( x )

* Binary Relational Operations
     - JOIN (several variations of JOIN exist)
     - DIVISION
     
* Additional Relational Operations
     - OUTER JOINS, OUTER UNION
     - AGGREGATE FUNCTIONS (These compute summary of information: for example, SUM, COUNT, AVG, MIN, MAX)

<hr>

**`Unary Relational Operations : SELECT`**

The SELECT operation denoted by (sigma) is used to select a subset of the tuples from a relation based on a selection condition.
        
         - الأمر Select من النوع Unary Relational Operations ويرمز له بالرمز Sigma ويستخدم لاختيار صفوف محددة من جدول (Relation) معين بناءا علي شرط معين .
         - ممكن نستخدم اكتر من شرط بردو.
         - Sigma <selection condition>(R) where R refer to Relation Name and the condition putted between angle brackets .
         - ممكن نستخدم في الشرط or / and .
  

**Example : <br>**
Select the EMPLOYEE tuples whose department number is 4:
Sigma DNO = 4 (EMPLOYEE)<br>    
         
    في المثال الموضح عندي Relation اسمها Employee فيها اكتر من Rows or Tuples فبختار منها كل ال Tuples اللي بيعملوا في ال Department اللي رقمه 4 وبعدين ارجع الداتا دي في صورة Relation .


**`Unary Relational Operations: PROJECT`**


PROJECT Operation is denoted by (pi) 

This operation keeps certain columns (attributes) from a relation and discards the other columns.

PROJECT creates a vertical partitioning


![](images\exampe.png)
         
    في هذا المثال يوجد Relation اسمها Employee والمطلوب اختيار ثلاث اعمدة منها وهم العمود الخاص بال Lname,Fname,Salary . 
       
- The general form of the project operation is:

       pi <attribute list> (R)
       (pi) is the symbol used to represent the project operation
       <attribute list> is the desired list of attributes from relation R. 
       The project operation removes any duplicate tuples


<hr>

`Relational Algebra Operations From Set Theory`

**UNION Operation**

- Binary operation, denoted by $\bigcup$ .

- The result of R $\bigcup$ S, is a relation that includes all tuples that are either in R or in S or in both R and S .
- Duplicate tuples are eliminated .
- The two operand relations R and S must be “type compatible” (or UNION compatible) .
- R and S must have same number of attributes .
- Each pair of corresponding attributes must be type compatible (have same or compatible domains) .

      كل عمودين هنجيب الاتحاد بينهم لازم يكون لهم نفس ال Datatype  أو نفس ال Domains ودا مفهوم Type compatible


**INTERSECTION**
- INTERSECTION is denoted by $\bigcap$ . 
- The result of the operation R $\bigcap$  S, is a relation that includes all tuples that are in both R and S
- The attribute names in the result will be the same as the attribute names in R
- The two operand relations R and S must be “type compatible”


**SET DIFFERENCE**
- SET DIFFERENCE (also called MINUS or EXCEPT) is denoted by – 
- The result of R – S, is a relation that includes all tuples that are in R but not in S .
- The attribute names in the result will be the same as the attribute names in R .
- The two operand relations R and S must be “type compatible” .


![](images\example1.png)

a
- first relation (student)
- second relation (instructor)

b
- student $\bigcup$ instructor

c
- student $\bigcap$ instructor

d
- student - instructor

e

- instructor - student

<hr>

**CARTESIAN PRODUCT**

CARTESIAN (or CROSS) PRODUCT Operation

- This operation is used to combine tuples from two relations in a combinatorial fashion.
- Denoted by R(A1, A2, . . ., An) x S(B1, B2, . . ., Bm).
- Result is a relation Q with degree n + m attributes:
  - Q(A1, A2, . . ., An, B1, B2, . . ., Bm), in that order.

- The resulting relation state has one tuple for each combination of tuples—one from R and one from S. 
Hence, if R has nR tuples (denoted as |R| = nR ), and S has nS tuples, then R x S will have nR * nS tuples.
- The two operands do NOT have to be "type compatible”.

<hr>

`Binary Relational Operations`

**JOIN**

JOIN Operation

![alt text](image.png)
- The sequence of CARTESIAN PRODECT followed by SELECT is used quite commonly to identify and select related tuples from two relations
- A special operation, called JOIN combines this sequence into a single operation
- This operation is very important for any relational database with more than a single relation, because it allows us combine related tuples from various relations 
- The general form of a join operation on two relations R(A1, A2, . . ., An) and S(B1, B2, . . ., Bm) is:
<mark>`R<join condition>S`<mark>
- where R and S can be any relations that result from general relational algebra expressions.


      
      فكرة ال join operation تكون بين two Relation ولازم يكون في condition معين وينتج Relation جديدة فيها اكتر من  Attribute list عددهم يساوي مجموع ال Attribute list اللي في ال two relation ونوع ال join هنا اسمه EQUIJOIN Operation وفي نوع اخر من ال Join اسمه Natural join وفيه مبنحتاجش نكتب join condition ونكتفي بكتابة * between two Relations وعدد الاتربيوت فيه يكون عدد الاتربيوت اللي موجودة في ال R1 + عدد الاتربيوت اللي موجودة في R2 ومتكونش اتكررت في R1.
      وفي نوع اخر اسمه Left outer join ,Right outer  join ،Full Outer Join بيدرسوا ال matching اللي بيحصل بين ال two relations مثلا في ال left outer join بيدرس ال matching اللي بيحصل بين ال left relation and right relation ولكنه يكون مهتم اكتر بال tuples الموجودة في ال left relation وقد اي هي بت match ال tuples الموجودة في ال right ولو خلصنا واتبقي tuples مش بت match ال right relatin بننزل ال left relation attribute ونخلي الجزء ال right كله بيساوي null ونفس هذا الكلام بيحصل مع ال right outer join ,Full outer join.

![](images\NJ.png) 

This is Figure reprsent Natural Join operation between  two tables Dept_Locations and Deptartment . 

(join conition -->> Dnumber = Dnumber and it's equal in two relations ) Thus, I use * mark between two relations  Department and Dept_Locations without using join condition .

<hr>

**DIVISION**

Division Operation

[![Click Here](https://img.youtube.com/vi/video-id/0.jpg)](https://www.youtube.com/watch?v=Tc1cSrXQ0gE&list=PL37D52B7714788190&index=27)




<hr>

`Additional Relational Operations`


**Aggregate Functions and Grouping**

- A type of request that cannot be expressed in the basic relational algebra is to specify mathematical aggregate functions on collections of values from the database. 
- Examples of such functions include retrieving the average or total salary of all employees or the total number of employee tuples.
    - These functions are used in simple statistical queries that summarize information from the database tuples.
- Common functions applied to collections of numeric values include
     - SUM, AVERAGE, MAXIMUM, and MINIMUM.

- The COUNT function is used for counting tuples or values.



**Aggregate Function Operation**

- Use of the Aggregate Functional operation ℱ
- ℱMAX Salary (EMPLOYEE) retrieves the maximum salary value from the EMPLOYEE relation
- ℱMIN Salary (EMPLOYEE) retrieves the minimum Salary value from the EMPLOYEE relation
- ℱSUM Salary (EMPLOYEE) retrieves the sum of the Salary from the EMPLOYEE relation
- ℱCOUNT SSN, AVERAGE Salary (EMPLOYEE) computes the count (number) of employees and their average salary
     - Note: count just counts the number of rows, without removing duplicates


**Using Grouping with Aggregation**

- The previous examples all summarized one or more attributes for a set of tuples
     - Maximum Salary or Count (number of) Ssn
- Grouping can be combined with Aggregate Functions
- Example: For each department, retrieve the DNO, COUNT SSN, and AVERAGE SALARY
- A variation of aggregate operation ℱ allows this:
     - Grouping attribute placed to left of symbol
     - Aggregate functions to right of symbol
     - DNO ℱCOUNT SSN, AVERAGE Salary (EMPLOYEE)
- Above operation groups employees by DNO (department number) and computes the count of employees and average salary per department


      ال Aggregate Function عبارة عن دالة احصائية من خلالها اقدر احصل علي احصائيات مهمة من البياتات المخزنة داخل جدول معين داخل Relation معينة يعني.
      ولكن الاحصائية دي تكون بالنسبة ل Attribute list واحد فقط لعمود واحد يعني زي مثلا ال Salary اقدر اجيب ال max or min or sum Salary الخاص بالموظفين علي مستوي ال Relation كلها.
      وفي حاجة تانية اسمها Grouping وال Grouping هو اني بقسم البيانات الموجودة في الجدول بناءا علي Attribute list معين وبعدين اطبق ال Aggregate function زي مثلا تقسيمة ال Relation بناءا علي (Attribute معين ) وليكن رقم القسم  وبعدين لكل جروب بجيب ال Average salary للموظفين اللي في الجروب واجيب عدد الموظفين في كل جروب من خلال عمل count لل SSN .


[![Click Here](https://img.youtube.com/vi/video-id/0.jpg)](https://www.youtube.com/watch?v=NjhQZhysi6g&list=PL37D52B7714788190&index=28&pp=iAQB)