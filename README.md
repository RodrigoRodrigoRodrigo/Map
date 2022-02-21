package application;

import java.util.Map;
import java.util.TreeMap;

public class Program {
	
	public static void main(String[] args) {
		
		/*
		 * put(key, value); ele serve para inserir um elemento numa determinada chave, ai você pode atribuir um valor pra 
		 * essa chave.
		 * 
		 *  tem o remove(key); que você passa a chave.
		 *  
		 *  tem o containsKey(key); pra verificar se existe uma dada chave.
		 *  
		 *  e tem o get(key); que ele recupera um elemento pela chave.
		 *  
		 *  ele tem uma operação bacana que é o keySet(); ele retorna um set com as chaves contidas no map.
		 *  
		 *  tem tambem o values(); que retorna uma coleção do tipo valor.
		 */
		
		Map<String, String> cookies = new TreeMap<>();
		/*
		 * como o tipo String ele ja tem implementado o equals e HashCode, e tambem o compareTo, eu posso usar o TreeMap
		 * aqui diretamente.
		 * 
		 * agora eu tenho uma estrutura para armazenas cookies.
		 */
		
		cookies.put("username", "maria");
		cookies.put("email", "maria@gmail.com");
		cookies.put("phone", "99771122");
		cookies.remove("email");
		cookies.put("phone", "99771133");
		/*
		 * eu inserindo um novo "phone", com um valor diferente, que que vai acontecer? ele vai sobreescrever o outro valor
		 * do "phone" de cima, por que o Map não aceita repetições, então ele vai ver que já existe esse "phone", e ele vai
		 * simplesmente gravar o novo valor pra lá. depois que executar o programa você vai notar que só existe um valor
		 * "phone" e o valor é o ultimo que eu inseri.
		 */
		
		System.out.println("Contains 'phone' key: " + cookies.containsKey("phone"));
		System.out.println("Phone number: " + cookies.get("phone"));
		System.out.println("Email: " + cookies.get("email"));
		System.out.println("Size: " + cookies.size());
		System.out.println("ALL COOKIES:");
		
		for (String key : cookies.keySet()) {
			System.out.println(key + ": " + cookies.get(key));
		}
	}
}

