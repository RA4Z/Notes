Checked Exceptions in [[Java]] are the exceptions verified by the compiler. Demanding that the developer treat these exceptions explicitly. Not treating them results in an compilation error.

#### Examples
- **IOException**: Occur when working with IO operations, like reading and writing files
- **SQLException**: Occur when interacting with databases and manipulating data
- **ClassNotFoundException**: Occur when the application try to load a class that is not available

```Java
import java.io.FileReader; 
import java.io.IOException;

public class ExemploChecked { 
	public static void main(String[] args) { 
		try { 
			FileReader arquivo = new FileReader("caminho_do_arquivo.txt"); 
			// Operações com o arquivo } 
		catch (IOException e) { 
			System.out.println("Ocorreu uma IOException: " + e.getMessage()); 
		} 
	} 
}
```
