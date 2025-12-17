Unchecked Exceptions in [[Java]], can't be verified during the compiling time, only during the running time. That means that the developer doesn't need to treat them explicitly, although it is highly recommended.
#### Examples
- **NullPointerException**: Occur when the code tries to access an object that wasn't initialized
- **ArrayIndexOutOfBoundsException**: Occur when trying to access an nonexistent position in an array
- **ArithmeticException**: Occur when realizing invalid arithmetic's operations, like division per zero

```Java
public class ExemploUnchecked { 
	public static void main(String[] args) { 
		int numerador = 10; 
		int denominador = 0; 
		try { 
			int resultado = numerador / denominador;
			System.out.println("Resultado: " + resultado); 
			} 
		catch (ArithmeticException e) { 
			System.out.println("Erro de operação aritmética: " + e.getMessage()); 
		} 
	} 
}
```