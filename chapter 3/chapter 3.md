# `Data Modeling Using Entity-Relationship (ER)Model`
#### ER model هو مودل يوضح العلاقة بين ال entities وبعضها داخل نفس ال environment or organizations.

![](images\ER.png)

 الانتيتي هو الكيان اللي بحتفظ عنه ببيانات داخل الداتا.


![](images\A.png)

ال attribute هو وصف للبيانات اللبي بحتفظ عنها لكل كيان داخل قاعدة البيانات
او هي الصفات اللي بستخدمها عشان اوصف الانتيتي.

![](images\R.png)

ال relationship هو علاقة بين اتنين Entities او اكتر 

نفترض ان احنا شغالين في شركة الشركة فيها اكتر من انتيتز زي الموظفين والبروجكت والايفتس اللي الشركة بتعملها 
كل انتيتي المفروض يكون ليه اتربيوت تصفه يعني كل موظف ليه اسم وجنسية ونوع واي دي وهكذا وممكن الموظف الواحد يشارك في اكتر من بروجكت او يشارك في اكتر من ايفنت دا توضيح لمفهوم الرليشن شيب اللي بين اكتر من انتتي .

## `Types of Attributes:`
الاتربيوتس هي وصف الانتيتي 

![](images\AT1.png)

## Attribute  can be divided into two types :
* simple
* composite <br>
النوع السيمبل هو نوع يحتمل قيمة واحدة مجردة لا أكثر ولا أقل زي النوع كدا male or female.
 نوع الثاني يحتمل اكتر من قيمة زي مثلا ال address العنوان اقدر اوصفه بأكتر من صفة.

![](images\AT2.png)

## Also Attribute  can be divided into two types :
* single valued
* Multi valued <br>
النوع الاول يحتمل قيمة واحدة فقط لا أكثر ولا أقل زي مثلا الرقم القومي بيكون مميز لكل شخص او النوع.<br>
النوع الثاني ممكن الاتربيوت يكون ليه اكتر من قيمة زي مثلا  انتيتي له اتربيوت تسمي qualfictions وال qualficition يندرج تحتها اكتر من مؤهل زي البكالريوس والماجستير والدكتوراه.

## Also Attribute  can be divided into two types :

![](images\AT3.png)

النوع دا يكون كومبلكس يعني بيكون mutlivalued and composite يعني باختصار الاتربيوت الواحدة بيندرج تحتها اكتر من attribute.


## Also Attribute  can be divided into two types :
* Stored Attribute
* Derived Attribute
<br>
النوع الاول بينطلب قيمته من المسخدم علشان يتم تخزينها في قاعدة البيانات زي مثلا تارخ الميلاد ومن خلال تاريخ الميلاد يمكن استنتاج العمر فنا هنااستنتجت العمر لذلك فهو Derived Attribute.

![](images\AT4.png)


# `Entity Relationship (ER) Model`

![](images\ERmodel.png)

الانتيتي يمثل بشكل مستطيل والاتربيوت يمثل بشكل بيضاوي.
<br>
الانتيتي الواحد بيكون ليه اكتر من اتربيوت وممكن الاتربيوت دي تكون كي اتربيوت او مش شرط بس لو الانتيتي ملهوش كي اتربيوت يبقي اسمه weak entity وفي هذه الحالة يتم كتابة اسم الانتيتي داخل double rectangle وغالبا ما يكون الويك انتيتي مرتبط بي انتيتي اخر.
<br>
multi valued attribute يمثل بشكل بيضاوي بس double زي ال phone  كدا وبيكون ليه اكتر من قيمة.
<br>
الاتربيوت اللي اسمه address نوعه composite attribute.

![](images\WE.png)

<hr>

## Relationship between Entities

Types of Relationship :
* Binary Relationship
* Ternary Relationship
* Recursive Relatioship
<br>
.النوع الاول يربط بين اتنين انتيتز
 <br>
 .النوع التاني يربط بين تلاتة انتيتز
<br>
.النوع الثالت موضح بالشكل

![](images\RelationShip.png)


![](images\RecursiveRelationhip.png)

## Constriants on Relationship

![](images\cardinality.png)


## `Exampe to illustate the ER model`

![](images\Example.png) 

