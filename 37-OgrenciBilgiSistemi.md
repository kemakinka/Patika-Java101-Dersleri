
### Teacher Sınıfı

```
public class Teacher {
    String name;
    String mpno;
    String branch;

    Teacher(String name, String mpno, String branch) { 
        this.name = name; 
        this.mpno = mpno; 
        this.branch = branch; 

    }
}

```
### Studen Sınıfı

```
public class Student {
    String name;
    String stuNo;
    int classess;
    Course math;
    Course physics;
    Course chemistry;
    Course vivaMath;
    Course vivaPhy;
    Course vivaChm;
    double average;
    boolean isPass;

    Student(String name, int classes, String stuNo, Course math, Course physics, Course chemistry, Course vivaMath,
            Course vivaChm, Course vivaPhy) {
        this.name = name;
        this.stuNo = stuNo;
        this.classess = classes;
        this.math = math;
        this.physics = physics;
        this.chemistry = chemistry;
        this.vivaMath = vivaMath;
        this.vivaChm = vivaChm;
        this.vivaPhy = vivaPhy;
    }

    public void addBulkExamNote(int math, int physics, int chemistry, int vivaMath, int vivaPhy, int vivaChm) {
        if (math >= 0 && math <= 100) {
            this.math.note = math;
        }
        if (physics >= 0 && physics <= 100) {
            this.physics.note = physics;
        }
        if (chemistry >= 0 && chemistry <= 100) {
            this.chemistry.note = chemistry;
        }
        if (vivaMath >= 0 && vivaMath <= 100) {
            this.vivaMath.note = vivaMath;
        }
        if (vivaPhy >= 0 && vivaPhy <= 100) {
            this.vivaPhy.note = vivaPhy;
        }
        if (vivaChm >= 0 && vivaChm <= 100) {
            this.vivaChm.note = vivaChm;
        }


        if (this.math.note == 0 || this.physics.note == 0 || this.chemistry.note == 0) {
            System.out.println("The notes are not fully entered");
        }
        else {
            this.isPass = isCheckPass();
            printNote();
            System.out.println("Average : " + this.average);
            if (this.isPass) {
            System.out.println("Passed The Class. ");
            }
            else { System.out.println("Failed The Class.");
            }
        }
    }

    public boolean isCheckPass() {
        calcAverage();
        return this.average > 55;
    }

    public void calcAverage() {
        this.average = (((this.physics.note * 0.8) + (this.vivaPhy.note * 0.2)) +
                        ((this.math.note * 0.8) + (this.vivaMath.note)) +
                        ((this.chemistry.note * 0.8) + (this.vivaChm.note))) / 3;

    }

    public void printNote() {
        System.out.println("=========================");
        System.out.println("Student : " + this.name);
        System.out.println("Math Grade : " + this.math.note);
        System.out.println("Math Viva Grade : " + this.vivaMath.note);
        System.out.println("Physics Grade : " + this.physics.note);
        System.out.println("Physics Viva Grade : " + this.vivaPhy.note);
        System.out.println("Chemistry Grade : " + this.chemistry.note);
        System.out.println("Chemistry Viva Grade : " + this.vivaChm.note);

        }
}

```

### Course Sınıfı

```
public class Course {
    Teacher courseTeacher;
    String name;
    String code;
    String prefix;
    int vivaMath;
    int vivaPhy;
    int vivaChm;
    int note;


    Course(String name, String code, String prefix){
        this.name = name;
        this.code = code;
        this.prefix = prefix;
        this.courseTeacher = courseTeacher;
        this.note = 0;
    }


    public void addTeacher(Teacher t){
        if (this.prefix.equals(t.branch)) {
            this.courseTeacher = t; System.out.println("The operation is successful"); }
        else { System.out.println(t.name + " Academician cannot teach this course."); }

    }

    public void printTeacher(){
        if (courseTeacher != null) {
            System.out.println(this.name + " Academician of the course: " + courseTeacher.name);
        }
        else {
            System.out.println(this.name + " to the course no Academician has been appointed.");
        }

    }

}
```

### Main Sınıfı

```
public class Main {
    public static void main(String[] args) {
        Course math = new Course("Math", "MAT101","MAT");
        Course physics = new Course("Physics", "PHY101", "PHY");
        Course chemistry = new Course("Chemistry","CHM101", "CHM");
        Course vivaMAth = new Course("Math", "MAT101","MAT");
        Course vivaPhy = new Course("Physics", "PHY101", "PHY");
        Course vivaChm = new Course("Chemistry","CHM101", "CHM");

        Teacher t1 = new Teacher("Rob","90123","MAT");
        Teacher t2 = new Teacher("Jenny", "90456", "PHY");
        Teacher t3 = new Teacher("Barbara", "90789", "CHM");

        math.addTeacher(t1);
        physics.addTeacher(t2);
        chemistry.addTeacher(t3);

        Student s1 = new Student("Jack", 4, "01", math, physics,chemistry,vivaMAth,vivaPhy,vivaChm);
        s1.addBulkExamNote(50,20,40,50,60,80);
        s1.isCheckPass();

        Student s2 = new Student("Oliver",4,"02",math, physics,chemistry,vivaMAth,vivaPhy,vivaChm);
        s2.addBulkExamNote(100,50,40,60,40,70);
        s2.isCheckPass();

        Student s3 = new Student("Oscar",4,"03",math,physics,chemistry,vivaMAth,vivaPhy,vivaChm);
        s3.addBulkExamNote(50,20,40,20,10,30);
        s3.isCheckPass();

    }
}
```
