## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

ActiveRecord is a SQL based interface between Ruby and a database
  
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

Team.all, Team.find(:id), Team.where(column_name: value)/Access given through Active Record

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

Team.find(4).name  /  Owner.find(Team.find(4).owner_id)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

Team.find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

Not sure how to include a schema diagram in markdown...or maybe I'm not understanding what a schema diagram is.
```
class Student
  has_many :classroom_assignments
  has_many :teachers, through: :classroom_assignments
end

class Teacher
  has_many :classroom_assignments
  has_many :students, through: :classroom_assignments
end

class ClassroomAssignment
  belongs_to :students
  belongs_to :teachers
end

```
6. Define foreign key, primary key, and schema.

Foreign key: A reference to the primary key of another table
Primary key: A unique id for each row or a table
Schema: file that contains all table info. NO EDITING ALLOWED

7. Describe the relationship between a foreign key on one table and a primary key on another table.

A foreign key on one table points to a primary key on another table. If the relationship is effectively definied in the models, the foreign key allows access from the table row with the foreign key directly to the associated row information on the table with the primary key. 

8. What are the parts of an HTTP response?

A request contains the verb, params, and url. Not actually sure what a response includes. Maybe html/erb and whatever data is carried inside them?

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.

find, find_by, where. They find a row by id, find the first row that matches whatever attribute entered, and find all rows that match the attribute entered, respectively.

2. Name your three favorite ActiveRecord rake tasks and describe what they do.

db:create (creates a database), db:migrate (runs migrations), db:seed (creates a development database populated with info found in the seed file)

3. What two columns does `t.timestamps null: false` create in our database?

Apparently rails 5.1.1 doesn't use this. It just says t.timestamps. And I think it creates a 'created at' column. Don't remember what the other is.

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?

I assume one school has many teachers (unless it's college in modern times and then it's a many to many relationship because colleges often hire part-time only)

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

Again, not sure how to draw a diagram in markdown. 
```
class School
  has_many :teachers
end

class Teacher
  belongs_to :school
end
```
6. Give an example of when you might want to store information besides ids on a join table.

actors/movies/join-table:contracts

7. Describe and diagram the relationship between patients and doctors.

```
class Doctor
  has_many :appointments
  has_many :patients, through: :appointments
end

class Patient
  has_many :appointments
  has_many :doctors, through: :appointments
end

class Appointments
  belongs_to :doctors
  belongs_to :patients
end

```

8. Describe and diagram the relationship between museums and original_paintings.
```
class Museum
  has_many :original_paintings
end

class OriginalPainting
  belongs_to :museum
end
```
9. What could you see in your code that would make you think you might want to create a partial?

repetition in erb/html
