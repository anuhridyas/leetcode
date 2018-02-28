public class Sample {

    public static String markdownParser( String markdown ) {
        int i =0 ;
        if(markdown==null || markdown.length()==0){
            return "";
        }
        char[] array= markdown.toCharArray();
        while(i < markdown.length() && array[i]!=' '){
            i++;
        }
        if(i == markdown.length()) {
            return "";
        }
        return "<h" +i+">" +markdown.substring(i+1) +"</h"+i+">";
    }

    public static void main(String[] args){
        Sample s =new Sample();

        markdownParser("# header");

    }
}
