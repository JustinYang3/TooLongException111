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


# 11.2 main
		Scanner input = new Scanner(System.in);
		String newString = "";
		System.out.println("enter string or DONE when finished");
		String userInput = "";
		while(!userInput.equalsIgnoreCase("DONE"))
		{
			newString+=userInput+"\t";
			userInput = input.nextLine();
			
			if(userInput.length()>=20)
			{
				try {
					throw new StringTooLongException();
				}
				catch (StringTooLongException ex) {
					System.out.print(ex.getMessage()+"\nEnter a string. Be aware that the limit is 20 characters long.\n");
					userInput="";
				}
			}
		}
		System.out.println("The letters are :");
		System.out.println(newString);
	}
}
