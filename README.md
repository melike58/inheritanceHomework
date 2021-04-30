# inheritanceHomework
public  class User {

    public  void userLogin()
    {
        System.out.println("Kullanıcı turunu seciniz : 1)Instuctor 2)Student");
    }

}




public class User {
    public User() { /* compiled code */ }

    public void userLogin() { /* compiled code */ }
}


public class Instructor extends User{

    public void userLogin()
    {
        System.out.println("Instructor olarak giris yapildi...");
    }
}




public class Student extends User{

    public void userLogin(){
        System.out.println("Student olarak giris yapildi...");
    }



}



public class UserManager {

    public void login(User user){
        System.out.println("Giris Yapidi");
        user.userLogin();
    }
    
}



public class InstructorManager extends UserManager{


    public void login(User user) {

        System.out.println("Instructor olarak giris yapildi...");
        user.userLogin();

    }

    public void homeworkAdd(){

        System.out.println("Odev Sisteme Eklendi...");

    }
    
    

}





public class StudentManager extends UserManager{


    public void login(User user) {
        System.out.println("Student olarak giris yapildi...");
        user.userLogin();
    }
    public void homeworkNew(){
        System.out.println("Yeni odeviniz var...");
    }


}


public class Main {

    public static void main(String[] args) {
        UserManager userManager = new UserManager();
        userManager.login(new Instructor());

        InstructorManager instructorManager = new InstructorManager();
        instructorManager.homeworkAdd();

        StudentManager studentManager = new StudentManager();
        studentManager.homeworkNew();
    }
}







