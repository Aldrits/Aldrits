# This is a sample Python script.
# Developing Point of Sale System.

Cashier_name = input("Cashier_name: ")
print()
print("Point of Sales System:")
print("GROUP 4 RESTAURANT MENU:")

# Declaration of constant and variables
print("===============|*MENU*|===================================")
print("BROWNIES:-----.40")
print("ICECREAM:------.50 ")
print("MANGO_FLOAT:----->60:" )
print("HALO_HALO:----->70" )
print("APPLEPIE:------>50.95" )
print("=============|*Customer's*|=================================")
customer = input("Customer name: ")
print()
print("======ENTER THE QUANTITY YOU WANT======")
BROWNIES = int(input("1.How many Brownies you want---->40.50:"))
ICECREAM = int(input("2.How many ICECREAM you want---->50.50:"))
MANGO_FLOAT = int(input("3.How many MANGO_FLOAT you want--->60.90:"))
HALO_HALO = int(input("4.How many HALO_HALO you want---->70.95:"))
APPLEPIE = int(input("5.APPLE_PIE You want--->50.60:"))
print()
item = ((BROWNIES * 40.50) + (ICECREAM * 50.50) + (MANGO_FLOAT * 60.90) + (HALO_HALO * 70.95) + (APPLEPIE * 50.60))
# Declaration of operation and math
if item > 0:
     print("Total: ","%6.2f" % item)
     receive=int(input("money_receive: "))
     if receive >= item:
        print(""*10)
        print("=================Total Bill System=====================")
        print("=======================================================")
        if BROWNIES > 0:
            print("BROWNIES: ", BROWNIES, " =====> Pesos", BROWNIES * 40.50)
        if ICECREAM > 0:
            print("ICECREAM: ", ICECREAM, " =====> Pesos", ICECREAM * 50)
        if MANGO_FLOAT> 0:
            print("MANGO_FLOAT: ", MANGO_FLOAT, " ======> Pesos", MANGO_FLOAT * 60)
        if HALO_HALO > 0:
            print("HALO_HALO : ", HALO_HALO , "=====> Pesos", HALO_HALO * 70)
        if APPLEPIE > 0:
            print("APPLEPIE: ", APPLEPIE, " =====> Pesos", APPLEPIE * 50)



        print("Customer: ", customer)
        print("Total_Orders: ", item)
        print("Money_receive: ", receive)
        print("Customer's Change: ", receive - item)
        print("==========================================================")
        print("Cashier_name: ", Cashier_name,       "9/2/2022")
        print("===========Thank You Come Again===========================")

     elif receive != item:
        print()
        print("INSUFFICIENT MONEY")
quit()
You sent
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.util.Scanner;
import java.util.concurrent.ThreadLocalRandom;

public class OnlineCafeOrder {

    static String costumer_name,costumer_address;
    static int taro_quantity,matcha_quantity,honeydew_quantity,strawberry_quantity,coffe_quantity;

    static int taro_quantity_price,matcha_quantity_price,honeydew_quantity_price,strawberry_quantity_price,coffe_quantity_price,total_price;
    static int costumerIDNum;

    static void insert_order(Scanner sc){
        try {
            total_price = taro_quantity_price + matcha_quantity_price + honeydew_quantity_price + strawberry_quantity_price + coffe_quantity_price;

            Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/milktea", "root","topitagupa09155524404");
            PreparedStatement order = connection.prepareStatement("INSERT INTO order_table (idorder_table,costumerName,costumerAddress,taro_quantity,match_quantity,honeydew_quantity,strawberry_quantity,coffe_quantity,total_price) VALUES(?,?,?,?,?,?,?,?,?)");

           costumerIDNum = (ThreadLocalRandom.current().nextInt(1000,9999));
           order.setInt(1,costumerIDNum);
           order.setString(2,costumer_name);
           order.setString(3,costumer_address);
           order.setInt(4,taro_quantity);
           order.setInt(5,matcha_quantity);
           order.setInt(6,honeydew_quantity);
           order.setInt(7,strawberry_quantity);
           order.setInt(8,coffe_quantity);
           order.setInt(9,total_price);
           order.executeUpdate();


        }catch (Exception e){
            e.printStackTrace();
        }
    }

    static void order_receipt(Scanner sc){
        try {
            Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/milktea", "root","topitagupa09155524404");
            PreparedStatement costumer_number_order = connection.prepareStatement("SELECT * FROM order_table WHERE idorder_table = ?");

            costumer_number_order.setInt(1, costumerIDNum);
            ResultSet costumer_receipt = costumer_number_order.executeQuery();

            if (costumer_receipt.next()){
                System.out.println("|========================================|");
                System.out.println("|Costumer Order Number: " + costumer_receipt.getInt("idorder_table"));
                System.out.println("|Costumer Name: " + costumer_receipt.getString("costumerName"));
                System.out.println("|Costumer Address: " + costumer_receipt.getString("costumerAddress"));

                int receipt_taro_quantity  = costumer_receipt.getInt("taro_quantity");
                int receipt_matcha_quantity = costumer_receipt.getInt("match_quantity");
                int receipt_honeydew_quantity = costumer_receipt.getInt("honeydew_quantity");
                int receipt_strawberry_quantity = costumer_receipt.getInt("strawberry_quantity");
                int receipt_coffe_quantity = costumer_receipt.getInt("coffe_quantity");

                if(receipt_taro_quantity >= 1){
                    System.out.println("| TARO MILK TEA                    " +   receipt_taro_quantity);
                    System.out.println("|                                  " + taro_quantity_price + "\n|");
                }
                if(receipt_matcha_quantity >= 1 ){
                    System.out.println("| MATCHA MILK TEA                  " + receipt_matcha_quantity);
                    System.out.println("|                                  " + matcha_quantity_price + "\n|");
                }
                if(receipt_honeydew_quantity >= 1 ){
                    System.out.println("| HONEYDEW MILK TEA                " + receipt_honeydew_quantity);
                    System.out.println("|                                  " + honeydew_quantity_price + "\n|");
                }
                if(receipt_strawberry_quantity >= 1 ){
                    System.out.println("| STRAWBERRY MILK TEA              " + receipt_strawberry_quantity);
                    System.out.println("|                                  " + strawberry_quantity_price + "\n|");
                }
                if(receipt_coffe_quantity >= 1 ){
                    System.out.println("| COFFE MILK TEA                   " + receipt_coffe_quantity);
                    System.out.println("|                                  " + coffe_quantity_price + "\n|");
                }
                System.out.println("|TOTAL PRICE: " + costumer_receipt.getInt("total_price"));
                System.out.println("|========================================|");
                System.exit(0);
            }

        }catch (Exception e){
            e.printStackTrace();
        }
    }

    static void cancel_order(Scanner sc){
        try {
            Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/milktea", "root","topitagupa09155524404");
            PreparedStatement cancel_order = connection.prepareStatement("DELETE FROM order_table WHERE idorder_table = ?");

            boolean delete_boolean;
            while (true){
                delete_boolean = false;
                try {
                    System.out.print("Enter Costumer Order Number: ");
                    int numberOrder = sc.nextInt();
                    cancel_order.setInt(1,numberOrder);

                    int rows = cancel_order.executeUpdate();
                    if(rows > 0){
                        System.out.println("Successfully Cancelling Order");
                    }else{
                        System.out.println("Costumer Order Number Not Found");
                    }

                }catch (Exception e){
                    delete_boolean = true;
                    System.out.println("Costumer Order Number Not Found");
                    sc.next();
                }
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Welcome to Milk Tea Shop Online Ordering");
        taro_quantity = 0;
        matcha_quantity = 0;
        honeydew_quantity = 0;
        strawberry_quantity = 0;
        coffe_quantity = 0;

        while (true) {
            while (true) {
                System.out.print("Order Milk Tea/Cancel Order [O/C]: ");
                String oder_want = sc.nextLine().toLowerCase();
                if (oder_want.equals("o")) {
                    while (true){

                        System.out.println("|===========================|==================|");
                        System.out.println("|                           |                  |");
                        System.out.println("|        COMMAND            |      PRICE       |");
                        System.out.println("|                           |                  |");
                        System.out.println("|===========================|==================|");
                        System.out.println("| T - Taro Milk Tea         |       ₱ 100      |");
                        System.out.println("| M - Matcha Milk Tea       |       ₱ 150      |");
                        System.out.println("| H - Honeydew Milk Tea     |       ₱ 200      |");
                        System.out.println("| S - Strawberry Milk Tea   |       ₱ 250      |");
                        System.out.println("| C - Coffee Milk Tea       |       ₱ 300      |");
                        System.out.println("|===========================|==================|");

                        order:
                        while (true){
                            System.out.print("Order: ");
                            String order = sc.nextLine().toLowerCase();

                            if (order.equals("t")){
                                boolean taro_boolean;
                                while (true){
                                    try {
                                        taro_boolean = false;
                                        System.out.print("How Many Taro Milk Tea Order: ");

                                        taro_quantity = sc.nextInt();
                                        sc.nextLine();

                                        while (true){
                                            taro_quantity_price = taro_quantity * 100;
                                            System.out.print("You Want To Order More(Y/N): ");

                                            String anotherOrder = sc.nextLine().toLowerCase();

                                            if(anotherOrder.equals("y")){

                                                break order;
                                            } else if (anotherOrder.equals("n")) {

                                                System.out.print("Enter Name: ");
                                                costumer_name = sc.nextLine();
                                                System.out.print("Enter Address ");
                                                costumer_address = sc.nextLine();
                                                insert_order(sc);
                                                order_receipt(sc);

                                            }else{
                                                System.out.println("Invalid Command");
                                            }


                                        }
                                    }catch (Exception e){
                                        taro_boolean = true;
                                        System.out.println("Invalid Input");
                                        sc.next();
                                    }
                                }
                            } else if (order.equals("m")) {

                                boolean matcha_boolean;
                                while (true){
                                    try {
                                        matcha_boolean = false;
                                        System.out.print("How Many Taro Milk Tea Order: ");

                                        matcha_quantity = sc.nextInt();
                                        sc.nextLine();

                                        while (true){
                                            matcha_quantity_price = matcha_quantity * 150;
                                            System.out.print("You Want To Order More(Y/N): ");

                                            String anotherOrder = sc.nextLine().toLowerCase();

                                            if(anotherOrder.equals("y")){
                                                break order;
                                            } else if (anotherOrder.equals("n")) {

                                                System.out.print("Enter Name: ");
                                                costumer_name = sc.nextLine();
                                                System.out.print("Enter Address ");
                                                costumer_address = sc.nextLine();
                                                insert_order(sc);
                                                order_receipt(sc);

                                            }else{
                                                System.out.println("Invalid Command");
                                            }


                                        }
                                    }catch (Exception e){
                                        matcha_boolean = true;
                                        System.out.println("Invalid Input");
                                        sc.next();
                                    }
                                }

                            }else if (order.equals("h")) {

                                boolean honeydew_boolean;
                                while (true){
                                    try {
                                        honeydew_boolean = false;
                                        System.out.print("How Many Honeydew Milk Tea Order: ");

                                        honeydew_quantity = sc.nextInt();
                                        sc.nextLine();

                                        while (true){
                                            honeydew_quantity_price = honeydew_quantity * 200;
                                            System.out.print("You Want To Order More(Y/N): ");

                                            String anotherOrder = sc.nextLine().toLowerCase();

                                            if(anotherOrder.equals("y")){
                                                break order;
                                            } else if (anotherOrder.equals("n")) {

                                                System.out.print("Enter Name: ");
                                                costumer_name = sc.nextLine();
                                                System.out.print("Enter Address ");
                                                costumer_address = sc.nextLine();
                                                insert_order(sc);
                                                order_receipt(sc);

                                            }else{
                                                System.out.println("Invalid Command");
                                            }


                                        }
                                    }catch (Exception e){
                                        honeydew_boolean = true;
                                        System.out.println("Invalid Input");
                                        sc.next();
                                    }
                                }

                            }else if (order.equals("s")) {

                                boolean strawberry_boolean;
                                while (true){
                                    try {
                                        strawberry_boolean = false;
                                        System.out.print("How Many Strawberry Milk Tea Order: ");


                                        strawberry_quantity = sc.nextInt();
                                        sc.nextLine();

                                        while (true){
                                            strawberry_quantity_price = strawberry_quantity * 250;
                                            System.out.print("You Want To Order More(Y/N): ");

                                            String anotherOrder = sc.nextLine().toLowerCase();

                                            if(anotherOrder.equals("y")){
                                                break order;
                                            } else if (anotherOrder.equals("n")) {

                                                System.out.print("Enter Name: ");
                                                costumer_name = sc.nextLine();
                                                System.out.print("Enter Address ");
                                                costumer_address = sc.nextLine();
                                                insert_order(sc);
                                                order_receipt(sc);

                                            }else{
                                                System.out.println("Invalid Command");
                                            }
                                        }
                                    }catch (Exception e){
                                        strawberry_boolean = true;
                                        System.out.println("Invalid Input");
                                        sc.next();
                                    }
                                }

                            }else if (order.equals("c")) {


                                boolean coffe_boolean;
                                while (true){
                                    try {
                                        coffe_boolean = false;
                                        System.out.print("How Many Coffee Milk Tea Order: ");


                                        coffe_quantity = sc.nextInt();
                                        sc.nextLine();

                                        while (true){
                                            coffe_quantity_price = coffe_quantity * 300;
                                            System.out.print("You Want To Order More(Y/N): ");

                                            String anotherOrder = sc.nextLine().toLowerCase();

                                            if(anotherOrder.equals("y")){
                                                break order;
                                            } else if (anotherOrder.equals("n")) {

                                                System.out.print("Enter Name: ");
                                                costumer_name = sc.nextLine();
                                                System.out.print("Enter Address ");
                                                costumer_address = sc.nextLine();
                                                insert_order(sc);
                                                order_receipt(sc);

                                            }else{
                                                System.out.println("Invalid Command");
                                            }
                                        }
                                    }catch (Exception e){
                                        coffe_boolean = true;
                                        System.out.println("Invalid Input");
                                        sc.next();
                                    }
                                }

                            }else{
                                System.out.println("Invalid Keyword");
                                break;
                            }
                        }
                    }
                } else if (oder_want.equals("c")) {
                    cancel_order(sc);

                } else {
                    System.out.println("Invalid Keyword");
                }
            }
        }
    }
}
