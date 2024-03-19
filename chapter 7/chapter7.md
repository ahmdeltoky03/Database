# Chapter 7
# `Relational Database Design by ER- and EERR-to-Relational Mapping` 

## Chapter Goals
**ER-to-Relational Mapping Algorithm** 
- Step 1: Mapping of Regular Entity Types
-  Step 2: Mapping of Weak Entity Types
-  Step 3: Mapping of Binary 1:1 Relation Types
- Step 4: Mapping of Binary 1:N Relationship Types.
- Step 5: Mapping of Binary M:N Relationship Types.
- Step 6: Mapping of Multivalued attributes.
- Step 7: Mapping of N-ary Relationship Types.

**Mapping EER Model Constructs to Relations** 
- Step 8: Options for Mapping Specialization or Generalization.
- Step 9: Mapping of Union Types (Categories)



<hr>

      Figure(1)
      هذا الشكل يعبر عن Entity-Relationship  Diagram (EER diagram)
![](images\ER.png)



      Figure(2)
      هذا الشكل يعبر عن Relational Database Schema
![](images\RRDS.png)


    المطلوب دلوقتي تحويل ال ER الي Relational model فنا بحول كل Entity الي Relation وال Entity الواحد ممكن يكون ليه اكتر من Attribute وال Attribute  انواع مختلفة ممكن يكون composite attribute or multi valued attribute , attribute عادي .
    أثناء التحويل لا يتم كتابة ال composite attribute في ال Relation ولكن يتم كتابة ال Attribute اللي بيتكون منها زي مثلا في الشكل رقم 1 اثناء التحويل name فلا يتم كتابة name في الشكل التاني ولكن يتم كتابة هو كان بيتكون من اي  Fname , Minit, Lname وهكذا بردو مع ال multi valued attribute زي الل location لا يتم كتابته في ال Relation اللي اسمها Department ولكن يتم عمل Relation جديدة له هو وال key attribute الخاص بال Relation وتاخد اسم جديد .
    والعلاقات اللي بين ال Entities وبعضها اثناء تحويلها الي Relation يتم استبدالها بالأسهم .
    ويتم مراعاة ايضا ال cardinality ratio اثناء التحويل من ER to Relational model .
    



# If You want to see example [`click here` ](https://www.youtube.com/watch?v=YgfSj66UnNs&list=PL37D52B7714788190&index=13)


## Another Example 

This Figure(1) represent ER model . 

![](images\ER2.png)


This Figure(2) represent Relational model of ER model that in Figure(1) .

![](images\RM2.png)




<hr>

# `Mapping Specialization or Generalization`

- Option 8A: Multiple relations-Superclass and subclasses.
- Option 8B: Multiple relations-Subclass relations only.
- Option 8C: Single relation with one type attribute.
- Option 8D: Single relation with multiple type attributes.



**Option 8A: Multiple relations-Superclass and subclasses**

This Figure represent EER model. 

![](images\specialization.png)


This Figure represent Relational model.

![](images\solspecialization.png)


       
    يتم تحويل كل superclasses and subclasses الي Relation ويتم الربط بين ال subclass and superclass من خلال ال primary key الخاصة بال super class .


<hr>

**Option 8B: Multiple relations-Subclass relations only**


This Figure represent EER model. 

![](images\opB.png)

This Figure represent Relational model.

![](images\opB(R).png)

     
     يتم تحويل كل subclasses الي Relation وكل Relation يكون فيها ال local attribute الخاص بيها و ال attribute اللي تميز ال superclass.



<hr>

**Option 8C: Single relation with one type attribute**


This Figure represent EER model. 

![](images\specialization.png)


This Figure represent Relational model.

![](images\op3.png)
     
     
      في (Type Attribute)Job attribute واحد وعلي اساسه نشوف ال Entity هيتبع انهو Subclass .
      تستخدم في حالة Disjoint case .
      - Handle Disjoint subclasses.
      - There exist one Type attribute.


<hr>



**Option 8D: Single relation with multiple type attributes**

This Figure represent EER model. 

![](images\op4.png)


This Figure represent Relational model.

![](images\op4(R).png)

    
    الفكره هنا ان بستخدم النوع دا لما اكون في حالةال overlapping يعني ال entity الواحد ممكن يبقي member في اكتر من sub class في نفس الوقت .
    - There exist more than one type attribute.
    - Handle overlapping case

<hr>