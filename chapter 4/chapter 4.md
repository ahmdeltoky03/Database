# `chapter 4`
# `Enhanced Entity Relationship Model (EER)`
## Chapter outline :
* EER stands for Enhanced ER or Extended ER
* EER  model concepts
  - Include all modeling concepts of basic ER
  - Additional concepts
      * Subclasses and Superclasses
      * specialization and Generalization
      * Attribute and Relationship inheritance
* The additional EER concepts are used to model applications more completely
   - EER include some object-oriented  features such as inheritance and polymorphism.

<hr>

#### `Subclassses and Superclasses`
**Superclass**: A superclass (also known as a parent class or base class) is a class that is extended or inherited by other classes. It serves as a blueprint for its subclasses. Superclasses define common behaviors and attributes that subclasses can inherit and extend. They are more general and abstract in nature.

**Subclass**: A subclass (also known as a child class or derived class) is a class that inherits properties and behaviors from a superclass. Subclasses can add their own unique features or modify existing behaviors inherited from the superclass. They specialize and refine the functionalities defined in the superclass.

In summary, the main difference between a superclass and a subclass lies in their roles and relationships within the class hierarchy. Superclasses provide a foundation upon which subclasses are built, while subclasses inherit and extend the characteristics of their superclass.

     اي انتتي بيكون ليه اتربيوت تميزه وRelationship بيشارك فيها مع انتتي تانيين والانتيتي يمثل superclass وممكن الانتيتي الواحد يتكون من اكتر من subclass وال subclass بيورث من الانتيتي الكبير اللي هو ال superclass الاتربيوت الخاصة بيه والعلاقات اللي بيشارك فيها وبيكون ليه اتربيوت تانية بردو بس بتكون خاصة بيه لوحده بتكون local Attribute يعني   



<hr>

#### `Specialization and Generalization`

Specialization: Specialization is the process of defining subclasses based on a superclass, where each subclass represents a subset of the attributes and relationships of the superclass. It involves identifying specific characteristics or attributes that are unique to certain subsets of entities within a broader category. This allows for more specific modeling and representation of different types of entities. For example, in a university database, the superclass "Person" might be specialized into subclasses such as "Student" and "Faculty", each with their own specific attributes and relationships.

Generalization: Generalization is the opposite process of specialization. It involves identifying common characteristics or attributes among entities and combining them into a more general superclass. Generalization is used to abstract common features from multiple subclasses into a single entity type. It helps in simplifying the model and capturing shared properties among related entities. For instance, in a hierarchical database model, different types of employees (such as full-time, part-time, and contract employees) may be generalized into a common superclass "Employee", which captures attributes and relationships common to all types.

In summary, specialization focuses on identifying specific subsets of entities with unique characteristics, while generalization abstracts common features from multiple entities into a more general representation. Both concepts are important in database design for organizing and representing complex data structures.


     عملية التخصيص اننا بقسم ال superclass الي اكتر من subclass وكل subclass بيكون ليه attribute local ومش بالضروري ال subclass التاني يكون عارفها عكس عملية ال Generalization  اننا بجمع اكتر من انتتي(sub class) اشتركوا في نفس الصفات و نفس العلاقات ونجمعهم في super class واحد .  

![](images\Specialisation_1.jpg)
![](images\Generalisation_1.jpg)



<hr>

#### `The additional EER concepts are used to model applications more completely`
![](images\EER.png)
      
      هذا الشكل يمثل EER diagram فيه انتيتي superclass اللي هو ال EMPLOYEE وفيه اكتر من sub class اللي هو MANAGER,ENGINEER,TECHNICIAN,SECRETARY,HOURS_EMPLOYEE,SALARIED_EMPLOYEE وهنا السوبر كلاس له اكتر من اتربيوت زي الاسم والرقم القومي وتاريخ الميلاد والعنوان وكل subclass ليه Local Attribute + Attributes اللي بيورثها من السوبر كلاس. مفهوم ال d هنا انه Disjointness constraints انا ال Employee مينفعش غير انه يبقي واحد من التلاتة مثلا يا اما Engineer or Technician or Secretary مينفعش يبقي غير واحد فقط وهكذا بردو في الجزء اليمين مينفعش غير انه يختار one sub class يا اما Hourly_Employee or Salaried_Employee .

<hr>