# Java_All_Framework_Annotations

## JPA Framework

#### Some of the main ones are @JoinColumn, @Table, @OneToOne, @OneToMany, @ManyToOne, @ManyToMany, and @Entity.


@Entity
#### Specifies that the class is an entity. This annotation can be applied on Class, Interface of Enums.

@Table: 
#### It specifies the table in the database with which this entity is mapped. 
#### In the example below the data will be stores in the “employee” table. 
#### Name attribute of @Table annotation is used to specify the table name.

@Column: 
#### Specify the column mapping using @Column annotation. 
#### Name attribute of this annotation is used for specifying the table’s column name.

@Id: 
#### This annotation specifies the primary key of the entity.

@GeneratedValue: 
#### This annotation specifies the generation strategies for the values of primary keys.

@Version: 
#### We can control versioning or concurrency using this annotation.

@OrderBy: 
#### Sort your data using @OrderBy annotation. In example below, it will sort all employees_address by their id in ascending order.

@Transient: 
#### Every non static and non-transient property of an entity is considered persistent, unless you annotate it as @Transient.

@Lob: 
#### Large objects are declared with @Lob.

@OneToOne
#### Employee and EmployeeDetail entities share the same primary key and we can associate them using @OneToOne and @PrimaryKeyJoinColumn.
#### In this case the id property of EmployeeDetail is not annotated with @GeneratedValue. 
#### The id value of Employee will be used for used for id of EmployeeDetail.

@ManyToOne
#### Many employees can share the same status. 
#### So, employee to employeeStatus is a many to one relation. 
#### @ManyToOne annotation can be used for the same.

@OneToMany
#### Employee to Communication will be a one-to-many relationship. 
#### The owner of this relationship is Communication so, we will use ‘mappedBy’ attribute in Employee to make it bi-directional relationship.

@PrimaryKeyJoinColumn
#### This annotation is used to associate entities sharing the same primary key.

@JoinColumn
#### @JoinColumn annotation is used for one-to-one or many-to-one associations when foreign key is held by one of the entities.

@JoinTable: 
#### @JoinTable and mappedBy should be used for entities linked through an association table.

@MapsId: 
#### Two entities with shared key can be persisted using @MapsId annotation.
