
public class Anagram {

	public static void main(String args[])
	{
		
		String s1="Yuho  ";
		String s2="yuho  ";
		
		
		String s="Pa lak";
		String b="Kalap ";
		
		
		String s11=SortMethod(s1.toLowerCase());
		String s21=SortMethod(s2.toLowerCase());
		System.out.println(s11.equals(s21) +" Both are same says sort method");
		
		System.out.println(CountMethod(s.toLowerCase(), b.toLowerCase())+ " Both are same says count method ");
		
		
	}
	public static String SortMethod(String s)
	{
			char[] ss= s.toCharArray();
		//	System.out.println(ss.toString());
			java.util.Arrays.sort(ss);
			return (new String(ss));
	}
	
	
	public static boolean CountMethod( String s1, String s2)
	{
		int [] charTotal=new int[256];
		char[] s1_array=s1.toCharArray();
		char[] s2_array=s2.toCharArray();
		for(char c:s1_array)
		{
			charTotal[c]++;
		}
		
		for(char c:s2_array)
		{
			if(--charTotal[c]<0)
				{
				 return false;
				}
			
			
		}
		return true;
		
	}
	
	
}
