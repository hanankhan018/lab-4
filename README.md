# lab-4
class task01{
    double radius;
    String color;
    public void calculateArea(){
        double area=(3.14)*radius*radius;
        System.out.println("arae of circle: "+area);
    }
    public static void main(String[] args){
        task01 red_circle=new task01();
        task01 green_circle=new task01();
         
         red_circle.radius=9.9;
          red_circle.color="red";
           green_circle.radius=44.8;
          green_circle.color="green";
           
red_circle.calculateArea();
green_circle.calculateArea();


System.out.println("radius of red circle: "+red_circle.radius);

System.out.println("radius of green circle: "+green_circle.radius);

    }
}



class task2{
    double radius;
    String color;
     task2(double radius,String color){
        this.radius=radius;
        this.color=color;
     }
    public double calculateArea(){
        double area=(3.14)*radius*radius;
        return area;
    }
    public static void main(String[] args){
        task2 red_circle=new task2(9.9,"red");
        task2 green_circle=new task2(44.8,"green");


System.out.println("radius of red circle: "+red_circle.radius);

System.out.println("radius of green circle: "+green_circle.radius);

System.out.println("Area of Red Circle: " + red_circle.calculateArea());
System.out.println("Area of Green Circle: " + green_circle.calculateArea());
    }
}








class task3{
    int balance;
    String AccountNumber;
    task3(int balance,String AccountNumber){
        this.balance=balance;
        this.AccountNumber=AccountNumber;
    }
     
    public void deposit(int amount){
        if(amount>0){
            balance+=amount;
            System.out.println("Deposited " + amount + " into account " + AccountNumber);
        }else{
         System.out.println("invalid amount");

        }

    }
    public void withdraw(int amount){
if(amount>0&&amount<=balance){
            balance-=amount;
            System.out.println("Withdrawn " + amount + " from account " + AccountNumber);
        }else{
         System.out.println("Insufficient amount");

        }
    }
    public void checkbalance(){
System.out.println("Account " + AccountNumber + " balance: " + balance);
    }
   
    public static void main(String[] args){
        task3 acc1=new task3(1000,"1");
        task3 acc2=new task3(500,"2");

acc1.checkbalance();
acc2.checkbalance();

   acc1.deposit(500);
 acc2.deposit(1500);
   
acc1.checkbalance();
acc2.checkbalance();

acc1.withdraw(500);
acc1.checkbalance();


acc2.withdraw(3000);




    }
}



class task4{
    String name;
     int yearOfJoining;
     String address;
    task4(String name, int yearOfJoining, String address) {
        this.name = name;
        this.yearOfJoining = yearOfJoining;
        this.address = address;
    }
    public void displayInfo() {
        System.out.println(name+" "+yearOfJoining+" "+address+" ");
    }


    public static void main(String[] args) {
        task4 emp1 = new task4("\tRobert\t", 1994, "\tWallsStreat");
        task4 emp2 = new task4("\tSam\t", 2000, "\tWallsStreat");
        task4 emp3 = new task4("\tJohn\t", 1999, "\tWallsStreat");
        System.out.println("\tName\t yearOfJoining\t address\t");
        System.out.println("------------------------------");

    emp1.displayInfo();
    emp2.displayInfo();
      emp3.displayInfo();

    }
   

}







class task5{
    int id;
    String name;
    double[] grades;
    task5(int id,String name,double[] grades){
        this.id=id;
        this.name=name;
        this.grades=grades;
    }
    
     void display_average_grade(){
        double sum=0;
        for(double num:grades){
            sum+=num;
        }
        double avg=sum/grades.length;
        System.out.println("average gardes of "+ name +" (ID :"+ id +" ) is: "+ avg);
    }
   double[] calcPercentage() {
        double[] percentages = new double[grades.length];
        for (int i = 0; i < grades.length; i++) {
            percentages[i] = (grades[i] / 200) * 100;
        }
        return percentages;
    }
   public String concat_ID_Name(){
    return id+"_"+name;
   
     }
      void displayStudentInfo() {
         System.out.println("\nStudent Details:");
        System.out.println("ID: " + id);
        System.out.println("Name: " + name);
display_average_grade();
double[] percentages = calcPercentage();
        System.out.print("Percentages: ");
        for (double percent : percentages) {
            System.out.print(percent + "% ");
        }
        System.out.println();
        System.out.println("Concatenated ID & Name: " + concat_ID_Name());

      }
   public static void main(String[] args){

   double[] grades1 = {180, 190, 175, 185, 195};
 double[] grades2 = {160, 170, 165, 175, 180};
    task5 obj1=new task5(220,"hanan khan",grades1);
    task5 obj2=new task5(221,"awais",grades2);

obj1.displayStudentInfo();
        obj2.displayStudentInfo();

   }
}



class task6 {
    int rows;
    int cols;
    int[][] matx; 
    task6(int rows, int cols) {
        this.rows = rows;
        this.cols = cols;
        matx = new int[rows][cols]; 
    }
    void get_matrix() {

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(matx[i][j] + " ");
            }
            System.out.println();
        }
    }
    void set_element(int row, int col, int value) {
            System.out.println("Invalid index!");
        
    }
    

    public static void main(String[] args) {
        task6 matrix1 = new task6(4, 3); 
        task6 matrix2 = new task6(3, 3); 
        matrix1.set_element(0, 0, 1);
        matrix1.set_element(0, 1, 2);
        matrix1.set_element(0, 2, 3);
        matrix1.set_element(1, 0, 4);
        matrix1.set_element(1, 1, 5);
        matrix1.set_element(1, 2, 6);
        matrix1.set_element(2, 0, 7);
        matrix1.set_element(2, 1, 8);
        matrix1.set_element(2, 2, 9);
        matrix1.set_element(3, 0, 10);
        matrix1.set_element(3, 1, 11);
        matrix1.set_element(3, 2, 12);

        matrix2.set_element(0, 0, 1);
        matrix2.set_element(0, 1, 2);
        matrix2.set_element(0, 2, 3);
        matrix2.set_element(1, 0, 4);
        matrix2.set_element(1, 1, 5);
        matrix2.set_element(1, 2, 6);
        matrix2.set_element(2, 0, 7);
        matrix2.set_element(2, 1, 8);
        matrix2.set_element(2, 2, 9);

        matrix1.set_element(1, 2, 3);//updating

        System.out.println("Matrix 1:");
        matrix1.get_matrix();
        
        System.out.println("Matrix 2:");
        matrix2.get_matrix();
    }
}
