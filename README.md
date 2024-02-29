class MobileStore
{
    String make;
    String model;
    String category;
    double price; 
    double discount;
    double netPrice;
 
    MobileStore()
    {
        this.make="Samsung";
        this.model="Galaxy S21";
        this.category="Smartphone"; 
        this.price = 80099.99; 
        this.discount = 0.15;
    }
 
    MobileStore(String make, String model, String category, double price, double discount)
    {
        this.make = make;
        this.model = model;
        this.category = category;
        this.price = price;
        this.discount = discount;
    }
 
    MobileStore(MobileStore obj, MobileStore obj1, MobileStore obj2)
    {
        this.make = obj.make;
        this.model = obj1.model;
        this.category = obj2.category;
        this.price = obj.price;
        this.discount = obj2.discount;
    }
 
    boolean getDetails()
    {
        System.out.println("***");
        System.out.println("company name: "+make);
        System.out.println("model: "+model);
        System.out.println("category: "+category);
        System.out.println("price: "+price);
        System.out.println("discount: "+discount);
        System.out.println("net price: "+calculateNetPrice()); 
        System.out.println("***");
        return true;
    }
 
    double calculateNetPrice()
    {
        netPrice = price - (price* discount); 
        return netPrice;
    }
}
 
public class mobile
{
    public static void main(String args[])
    {
        MobileStore mobile1 = new MobileStore();
        mobile1.getDetails();
 
        MobileStore iphone = new MobileStore("Apple", "iPhone 12", "Smartphone", 99999.99, 0.1);
        iphone.getDetails();
 
        MobileStore Samsung = new MobileStore("Samsung", "Galaxy S21", "Smartphone", 88899.99, 0.15);
        Samsung.getDetails();
 
        MobileStore Google = new MobileStore("Google", "Pixel 5", "Smartphone", 69999.99, 0.2);
        Google.getDetails();
 
        MobileStore mobile2 = new MobileStore(iphone,Samsung,Google); 
        mobile2.getDetails();
    }
 
 
}
 
Ouput:
***
company name: Samsung
model: Galaxy S21
category: Smartphone
price: 80099.99
discount: 0.15
net price: 68084.9915
***
***
company name: Apple
model: iPhone 12
category: Smartphone
price: 99999.99
discount: 0.1
net price: 89999.99100000001
***
***
company name: Samsung
model: Galaxy S21
category: Smartphone
price: 88899.99
discount: 0.15
net price: 75564.9915
***
***
company name: Google
model: Pixel 5
category: Smartphone
price: 69999.99
discount: 0.2
net price: 55999.992000000006
***
***
company name: Apple
model: Galaxy S21
category: Smartphone
price: 99999.99
discount: 0.2
net price: 79999.992
***

