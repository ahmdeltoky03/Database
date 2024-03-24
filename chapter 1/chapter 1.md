# (`Databases and Database Users`)
    A database is a collection of related data.By data data i mean facts that can be recorded and have implicit meaning.For example,consider the username,telephone number and address of the people you know.

    Database represent some aspect of the real world sometimes called the mini world or the universe of discourse(UOD).

  Examples:
  * Traditional database application
    #### -store textual and numeric information.
  * Multimedia database
    #### -store images ,audio clips and video.
  * Geographical information system
    #### -store and analyze maps,satellite images and weather data.
  * Data warehouses and online analytical processing systems.
    #### -extract and analyze useful business information from a large database.
    #### -support decision making. 
  
  # (`Database Management System(DBMS)`)
       It is a collection of programs that enable users  to create and maintain a database.
       It is General purpose software system that facilities the process of defining,manipulating,constructing and sharing databases among various users and application.
       نظام ادراة قواعد البيانات هو عبارة عن مجموعة من البرامج التي تمكن المستخدم من انشاء قاعدة البيانات والتعديل فيها وهذا النظام يسهل عمليات عديدة مثل انشاء قاعدة بيانات وتعريفها والتعامل معاها ومشاركتها بين اكتر من مستخدم وأبلكيشن

       Process:
       1-Definition: This process involves the specifying the data types,structure and constraints of the data that stored in the database.The descriptive information or database definition called is stored by DBMS in the form of database catalog called meta data.
       2-construction:in this process the data is stored by DBMS.
       3-Manipulation:in this process the user send request or queries to data base and the DBMS send response to him.A data base includes a function such as queries the data base to retrieve specific data,updating the data base to reflect changes in the mini world and generate reports from the data. 
       اي مسنخدم بيرسل كويري للداتا بيز والDBMS يرد عليه بالresponse.
       4-Sharing : Allow to various users to access the same data simultaneously.
       5-Transaction: data may be read or written into data base.
       اي عملية قراءة او كتابة من الداتا بيز.

## Protection includes:
* System protection:حماية لقاعدة البيانات من خلال عدم السماح لأي مستخدم بالدخول غير بالemail and password.
* Security protection:البيانات تظل محفوظة لو حصل اي مشكلة فالسيستم سواء مشكلة هارد وير او سوفت وير.

# (`Example -->> University Database`) 
# (`<قاعدة بيانات خاصة بجامعة>`)
      * information connects  students with their courses,classes and grades.
      Data Records:
      -Student
      -Course
      -Section
      -Grade Report
### This figure represent the Meta-Data  in the university database.
![Meta-Data](images\MD.png)
# (```Meta-Data describe the structure of Data Base```)
      * Construct University Database
      -store data to represent student,course,section and grade report.
      
      *Relationships among the records.

      *Manipulation involves querying and updating.

      قاعدة البيانات الخاصة بالجامعة يدخل اليها الدكتور والطالب ففي البداية كدا محتاجين نريكورد الداتا الخاصة بالطالب الواحد زي الاسم والعنوان والرقم القومي والايميل والباسورد والكورسات اللي مسجلها وكدا وههكذا نسجل اسم الدكتور واسم المقررات اللي بيدرسها والايميل الخاص به والباسورد ومحتاجين نشوف الداتا تايب الخاصة بكل ريكورد ونضع شروط لكل داتا العملية دي اسمها تعريق قاعدة البيانات DB Definition
      وبعد كدا نبتدي نبني القاعدة وفي هذة العملية يتم التخزين الفعلي للداتا الخاصة بكل طالب ودكتور ومحتاجين نكونكت بين الريكورد 
      وبعد مخزنا البيانات الخاصة بالطالب او الدكتور الطالب ممكن يعدل في البيانات انه ممكن يغير الباسورد مثلا او يغير تسجبل اي مقرر او ما شابه ذلك

![](images\DB1.png)
الصورة دي بتوضح انا كيوزر بتعامل مع قاعدة البيانات ازاي انا برسل للداتا بيز كويري بطلب منه استفسار اللي بيستقبل الاستفسار دا DBMS وبعدين في سوفت وير سيستم بيعمل تحليل للبروسيس دي وفي سوفت وير تاني بيكون ليه اكسس لمكانين مكان خاص بالميتا داتا اللي بيتخزن فيه database definition or descriptive information ومكان تاني نخزن فيه الداتا.وبعدين ال DBMS بيروح من خلال تحليلية للكويري يشوف الداتا المطلوبة وبعدين يروح يشوف الوصف الخاص بيها من ال الميتا داتا ويرسل الوصف ك respond لليوزر وبكدا يكون اليوزر حصل علي البيانات اللي هو عايزها.

<hr>

# (`Disadvantagesof file Processing`)
* Program-Data Depenecne.
* Duplication of Data.
* Limited Data sharing.
* Legency Development time.
* Excessive Program maintenance.
* 
قاعدة البيانات حلت مشاكل كتير جدا زي مشكلة تكرار الداتا والتعديل في الداتا كان بياخد وقت كتير ومكنتش بعرف اشارك الداتا مع اكتر من يوزر وعشان اعمل ابديت للداتا بعمل ابديت لكل النسخ اللي مكتوب عليها البرنامج.

![](images\DB2.png)

# `Characteristic of using Database Approch`
* # Self Describing of Data Base System. 
* # Data Abstraction.
      Data Abstraction : Allows program-Data independence and program operation indepenence.
      الداتا بيز بتستخدم data model عشان تطبف مفهوم ال data Abstraction.
* # Support a multiple view of the Data.
* # Sharing of Data and multiusers Transaction processing.



# `Database Administrators`
![](images\DBA.png)



# Actors in the Scene
# الأشخاص اللي بتعامل معاهم في الداتا بيز 
  - Database adminstrations
  - Database Designers
  - End users
  - Systems Analysts and Application Programmers


### Database adminstrations
هو الشخص المسؤل عن اي حاجة في الداتا بيز authorizing acess to database ,acquiring software and hardware resources as need.وهو المسئول عن اي مشكلة تحصل في قاعدة البيانات poor response time.

### Database Designers

![](images\Design.png)

### Systems Analysts and Application Programmers
الشخص اللي بيشوف الكويري اللي ممكن اليوزر يعملها علي السيستم  ويبدأ يضيفها.<hr>

# Workers behind the Scene
  - DBMS systems designers and implementers
   الشخص المسؤل عن عمل ديزاين للسيستم وعمل implemention لل DBMS module as a software backage.
  - Tools Developers 
  Design and implement tools
  - Operators and maintanence personal:
    responsible for running and maintanence hardware and software environment for the database system.  