// UniversityGraphDB

// Cypher code that simulates a University Database with (students, instructors, courses)

Create (:student {name: "Jood Wafa", Id: "2001", Major: "Computer Science"})
Create (:student {name: "Sara Khaled", Id: "2002", Major: "Data Science"})
Create (:student {name: "Ali Musa", Id: "2003", Major: "Software Engineering"})
Create (:student {name: "Ahmad Muhsen", Id: "2004", Major: "Computer Science"})
Create (:student {name: "Layan Abdullah", Id: "2005", Major: "Cyber Security"})
Create (:student {name: "Aya Samer", Id: "2006", Major: "Data Science"})
Create (:student {name: "Dania Fehmi", Id: "2007", Major: "Data Science"})
Create (:student {name: "Abdulrahman Abdullah", Id: "2008", Major: "Computer Engineering"})
Create (:student {name: "Sami Sameer", Id: "2009, Major: "Computer Science"})
Create (:student {name: "Dana Ghaleb", Id: "2010", Major: "Computer Engineering"})
Create (:student {name: "Ashraf Khaleel", Id: "2011", Major: "Software Engineering"})

Create (:instructor {name: "Rahaf Saleh", Id: "3001", Department: "Computer Science"})
Create (:instructor {name: "Fahd Jaber", Id: "3002", Department: "Computer Science"})
Create (:instructor {name: "Adil Kareem", Id: "3003", Department: "Computer Engineering"})
Create (:instructor {name: "Dana Mahmoud", Id: "3004", Department: "Computer Engineering"})
Create (:instructor {name: "Fadi Maher", Id: "3005", Department: "Software Engineering"})
Create (:instructor {name: "Hadeel Mustafa", Id: "3006", Department: "Data Science"})
Create (:instructor {name: "Rana Karam", Id: "3007", Department: "Basic Sciences"})


Create (:course {name: "Intro to CS", Id: "1001", Department: "Computer Science"})
Create (:course {name: "Physics 1", Id: "1002", Department: "Basic Sciences"})
Create (:course {name: "Calculus 1", Id: "1003", Department: "Basic Sciences"})
Create (:course {name: "Structured Programming", Id: "1004", Department: "Computer Science"})
Create (:course {name: "Digital Logic Design", Id: "1005", Department: "Computer Engineering"})
Create (:course {name: "Circuits 1", Id: "1006", Department: "Computer Engineering"})
Create (:course {name: "OOP", Id: "1009", Department: "Computer Science"})
Create (:course {name: "Database Systems", Id: "1010", Department: "Computer Science"})
Create (:course {name: "Artificial Intelligence", Id: "1008", Department: "Data Science"})

Match (n1: instructor {name: "Rahaf Saleh"}), (n2: course{name:"Intro to CS"})
Create (n1) -[:teaches {time:"14:00 - 15:00"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Fahd Jaber"}), (n2:course{name:"Intro to CS"})
Create (n1) -[:teaches {time:"9:00 - 10:00"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Fahd Jaber"}), (n2:course{name:"Intro to CS"})
Create (n1) -[:teaches {time:"14:00 - 15:30"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Rahaf Saleh"}), (n2:course{name:"Structured Programming"})
Create (n1) -[:teaches {time:"12:00 - 13:00"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Rana Karam"}), (n2:course{name:"Physics 1"})
Create (n1) -[:teaches {time:"13:00 - 14:00"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Adil Kareem"}), (n2:course{name:"Circuits 1"})
Create (n1) -[:teaches {time:"11:00 - 12:30"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Dana Mahmoud"}), (n2:course{name:"Digital Logic Design"})
Create (n1) -[:teaches {time:"8:00 - 9:00"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Hadeel Mustafa"}), (n2:course{name:"Artificial Intelligence"})
Create (n1) -[:teaches {time:"8:00 - 9:00"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Fadi Maher"}), (n2:course{name:"OOP"})
Create (n1) -[:teaches {time:"12:00 - 13:00"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Rana Karam"}), (n2:course{name:"Calculus 1"})
Create (n1) -[:teaches {time:"9:30 - 11:00"}]-> (n2)
With 1 as dummy

Match (n1:instructor{name: "Fade Maher"}), (n2:course{name:"Database Systems"})
Create (n1) -[:teaches {time:"11:00 - 12:00"}]-> (n2)
With 1 as dummy




Match (n1:student{name: "Jood Wafa"}), (n2:course{name:"Database Systems"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Sara Khaled"}), (n2: course{name:"Database Systems"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Sara Khaled"}), (n2: course{name:"Structured Programming"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Jood Wafa"}), (n2: course{name:"Artificial Intelligence"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Aya Samer"}), (n2: course{name:"Database Systems"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Ali Musa"}), (n2: course{name:"Artificial Intelligence"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Ahmad Muhsen"}), (n2: course{name:"OOP"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Ahmad Muhsen"}), (n2: course{name:"Digital Logic Design"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Layan Abdullah"}), (n2: course{name:"OOP"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Ashraf Khaleel"}), (n2: course{name:"OOP"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Abdulrahman Abdullah"}), (n2: course{name:"Digital Logic Design"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Abdulrahman Abdullah"}), (n2: course{name:"Circuits 1"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Sami Sameer"}), (n2: course{name:"Digital Logic Design"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Dana Ghaleb"}), (n2: course{name:"Calculus 1"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Dana Ghaleb"}), (n2: course{name:"Physics 1"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Layan Abdullah"}), (n2: course{name:"Calculus 1"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Dania Fehmi"}), (n2: course{name:"Physics 1"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Dana Ghaleb"}), (n2: course{name:"Intro to CS"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Dania Fehmi"}), (n2: course{name:"Intro to CS"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy

Match (n1: student{name: "Ali Musa"}), (n2: course{name:"Structured Programming"})
Create (n1) -[:takes]-> (n2)
With 1 as dummy


Match (n1: student{name: "Sara Khaled"}), (n2: student{name:"Jood Wafa"})
Create (n1) -[:partners {course: "Database Systems"}]-> (n2)
With 1 as dummy

Match (n1: student{name: "Jood Wafa"}), (n2: student{name:"Sara Khaled"})
Create (n1) -[:partners {course: "Database Systems"}]-> (n2)
With 1 as dummy

Match (n1: student{name: "Dana Ghaleb"}), (n2: student{name:"Dania Fehmi"})
Create (n1) -[:partners {course: "Intro to CS"}]-> (n2)
With 1 as dummy

Match (n1: student{name: "Dania Fehmi"}), (n2: student{name:"Dana Ghaleb"})
Create (n1) -[:partners {course: "Intro to CS"}]-> (n2)
