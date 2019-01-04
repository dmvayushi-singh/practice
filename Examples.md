public class Example {

    public static void main(String[] args) {
        Task obj = new Task();
        Task2 obj2 = new Task2();
        obj.start();
        try{
            Thread.sleep(13);
        }
        catch(Exception e){
        }
        obj2.start();
    }

    }


class Task extends Thread {

    public void run() {
        for (int i = 0; i <= 26; i++) {
            System.out.println(i++);
            try{
                Thread.sleep(1300);
            }
            catch(Exception e){
                System.out.println("this is exception.");
            }
        }
    }
}
class Task2 extends Thread{

    public void run(){
        for (int i = 0; i <= 12; i++) {
            System.out.println("it is a line" +""+ i);
            try{
                Thread.sleep(1300);
            }
            catch(Exception e){
                System.out.println("this is exception");
            }
        }
    }
}

