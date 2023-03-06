# Ejercicios-Java-

# Strings :
## 105:

~~~
    public static void main(String[] args) {

       String palabras = "abcd abc aabc baa abcaa";
       String encontrar = "aa";
       int contar = contarlasveces(palabras, encontrar);
       System.out.println(encontrar + " aparece " + contar + " veces en '" + palabras + "'");            
   }
  public static int contarlasveces(String palabras, String encontrar) {
       
       int position = 0;
       int contador = 0;
       int n = encontrar.length();
       while ((position = palabras.indexOf(encontrar, position)) != -1) {
           position = position + n;
           contador++;
       }
       return contador;
   }
  }

~~~


## 106:

~~~
   public static void main(String[] args) {

        String loQueRepite = "PHP";
        System.out.println("Lo que se debe repetir: "+loQueRepite);
        String resultado = repetir(loQueRepite, 7);
       System.out.println("\nDespues de reperirse 7 veces: "+resultado);
   }
public static String repetir(String loQueRepite, int num) {
       if (loQueRepite == null || loQueRepite.isEmpty()) {
           return "";
       }
       if (num <= 0) {
           return loQueRepite;
       }
       
       StringBuilder nuevaPal = new StringBuilder(loQueRepite.length() * num);
       for (int i = 1; i <= num; i++) {
           nuevaPal.append(loQueRepite);
       }
       return nuevaPal.toString();
   }
}
~~~



## 107:

~~~
public static void main(String[] args) {
        java.util.Scanner scanner = new java.util.Scanner(System.in);
        System.out.print("Introduce la cadena: ");
        String cadena = scanner.nextLine();
        System.out.print("Introduce el carácter a contar: ");
        
        char caracter = scanner.next().charAt(0);
        int contador = contarCaracter(cadena, caracter);
        System.out.println("El carácter '" + caracter + "' aparece " + contador + " veces en la cadena.");
    }
    
    public static int contarCaracter(String cadena, char caracter) {
        int contador = 0;
        for (int i = 0; i < cadena.length(); i++) {
            if (cadena.charAt(i) == caracter) {
                contador++;
            }
        }
        return contador;
    }

~~~

## 108:

~~~

    public static void main(String[] args) {	   
	    String palabra = "Marriposa";
		System.out.println(palabra);
		System.out.println("Tiene dos letras consecutivas: "+ comprobar(palabra));
		
    }
   public static boolean comprobar(String palabra) {
			for (int i=0;i<palabra.length()-1;i++)
			if (palabra.charAt(i)==palabra.charAt(i+1))
				return true;
		return false;
  }

~~~

## 109:


~~~

 public static void main(String[] args) {
   String text = "Hola maria mi llamo ama y tu como te llamas";
   System.out.println("Original text: " + text);
   System.out.println("\nAl reves palabras con longitud impar:\n" + test(text));
  
 }
 public static String test(String str) {
   String[] palabras = str.split(" ");
   
   for (int i = 0; i < palabras.length; i++) {
     if (palabras[i].length() % 2 != 0) {
       StringBuilder alReves = new StringBuilder(palabras[i]);
       palabras[i] = alReves.reverse().toString();
     }
   }
   return String.join(" ", palabras);
 }
    
~~~

## 110:

~~~

  public static void main(String[] args) {
   String texto = "fkjahljfffuuuu";
   System.out.println("Original String: " + texto);
   System.out.println("Numero de caracteres que se repiten masa de dos veces: " + comprobar(texto));
   }
 public static int comprobar(String text) {
   int contador = 0;
   while (text.length() > 0) {
     if (text.length() - text.replaceAll(text.charAt(0) + "", "").length() > 2) {
       contador++;
     }
     text = text.replaceAll(text.charAt(0) + "", "");
   }
   return contador;
 }
~~~

## 111:

~~~

 public static void main(String[] args) {
    Scanner leer = new Scanner(System.in);   
    System.out.println("Escribe la palabra: ");
    String text = leer.nextLine();
    System.out.println("Escribe lo que quieres eliminar: ");
    String palabra = leer.nextLine();
    System.out.println("Nueva frase\n"+test(text,palabra));
  }
  
 public static String test(String text, String word) 
  	{
	String resultado = text.replace(word, "");
	resultado = resultado.replaceAll("\\s+", " ");
	return resultado;
  }  
}

~~~

## 112:

~~~

public static void main(String[] args) {
     Scanner leer = new Scanner(System.in);
     System.out.println("Escribe una frase: ");
     String text = leer.nextLine();
     System.out.println("Escribe una palabra o frase: ");
     String palabra = leer.nextLine();
     System.out.println("Se encuentra o no \n" + test(text, palabra));
   }
   public static boolean test(String primeraCad, String segundaCad) {
     if (segundaCad.length() > primeraCad.length()) return false;
     if (segundaCad.isEmpty())
       return true;
     for (int i = 0; i < segundaCad.length(); i++) {
       if (!primeraCad.contains(String.valueOf(segundaCad.charAt(i))))
         return false;
     }
     return true;
   }

~~~

# Arryas Lits:

## 8:

~~~
  Collections.sort(list_Strings);

~~~
o método de la burbuja

## 9:

~~~

 public static void main(String[] args) {
 
List<Integer> originalList = new ArrayList<Integer>();
originalList.add(1);
originalList.add(2);
originalList.add(3);


List<Integer> newList = new ArrayList<Integer>();

for (int i = 0; i < originalList.size(); i++) {
    newList.add(originalList.get(i));
}

System.out.println("Lista original: " + originalList);
System.out.println("Nueva lista: " + newList);
 
 }
}
~~~

## 10:

~~~


~~~


