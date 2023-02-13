# TooLongException111
        Scanner input = new Scanner(System.in);
        String newString = "";
        System.out.println("enter string or done when finished");
        String userInput = input.nextLine();
        while(!userInput.equalsIgnoreCase("DONE"))
        {
        	if(userInput.length() >= 20)
        		throw new StringTooLongException();
                
        	newString+=userInput+" \t";
        	userInput = input.nextLine();
        }
        System.out.println("The letters are :");
        System.out.print(newString);
        
# String exception
class StringTooLongException extends Exception {
	public StringTooLongException (){
		super("Too many characters!");
	       
   }
}
