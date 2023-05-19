# Informacoesinvertexto
Todos meus dados do invertexto 




                                                                 MINHA CONTA NO GIT HUB 

https://github.com/Pamjune
email: pam.emilly@outlook.com
senha: 93903138Pam@

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
AULA 2- 15/04/2023
package br.com.arq.controller;

import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.ResponseBody;
import org.springframework.web.bind.annotation.RestController;

import br.com.arq.entity.Users;
import br.com.arq.repository.UsersRepository;

@ResponseBody
@RestController
@RequestMapping("/api")
public class UsersController {
 
	  @Autowired
	  private UsersRepository usersRepository;
	  
	   @PostMapping("/users")
	   public ResponseEntity<?> createUser(@RequestBody Users users){
		   try {
			Users resposta =   usersRepository.save(users);
			  if (resposta==null) {
				  throw new Exception("Nao gravou"); //va para o catch
			  }
			
			  return ResponseEntity.status(200).body(resposta);
			   
		   }catch(Exception ex) {
			 return ResponseEntity.status(500).body("error servidor internal");
		   }
	   }
	 
	   @GetMapping("/users")
	   public List<Users> findUsers(){
		   return usersRepository.findAll();
	   }
	
}


Eai cria aqui que e pra fofocar!



JAVA_HOME = C:\Program Files\Java\jdk1.8.0_202

JAVA_HOME = Até o JDK


PATH = + (os programas)  C:\Program Files\Java\jdk1.8.0_202\bin

====

 console
 
  java -version
  
  
=====

 mvn clean

 mvn clean install 

##
package br.com.arq.entity;

import java.io.Serializable;

import org.springframework.data.annotation.Id;
import org.springframework.data.mongodb.core.index.Indexed;
import org.springframework.data.mongodb.core.mapping.Document;
@Document(collection="users")
public class Users implements Serializable{
 
	private static final long serialVersionUID = 4919937187176204853L;
    @Id
	private String id;
	private String nome;
	@Indexed(unique=true)
	private String email;
	private String senha;
	private String status;
	
	public Users() {
		// TODO Auto-generated constructor stub
	}
	
	
	
	public Users(String id, String nome, String email, String senha, String status) {
		super();
		this.id = id;
		this.nome = nome;
		this.email = email;
		this.senha = senha;
		this.status = status;
	}



	@Override
	public String toString() {
		return "Users [id=" + id + ", nome=" + nome + ", email=" + email + ", senha=" + senha + ", status=" + status
				+ "]";
	}



	public String getId() {
		return id;
	}
	public void setId(String id) {
		this.id = id;
	}
	public String getNome() {
		return nome;
	}
	public void setNome(String nome) {
		this.nome = nome;
	}
	public String getEmail() {
		return email;
	}
	public void setEmail(String email) {
		this.email = email;
	}
	public String getSenha() {
		return senha;
	}
	public void setSenha(String senha) {
		this.senha = senha;
	}
	public String getStatus() {
		return status;
	}
	public void setStatus(String status) {
		this.status = status;
	}
	public static long getSerialversionuid() {
		return serialVersionUID;
	}
	
	
	
	
	
	
}

================================================================================================
JAVA_HOME = C:\Program Files\Java\jdk1.8.0_202

JAVA_HOME = Até o JDK

================================================================================================
PATH = + (os programas)  C:\Program Files\Java\jdk1.8.0_202\bin

================================================================================================

 console
 
  java -version
  
  
====================================================================================================

 mvn clean

 mvn clean install 

********************************************************************************************************************************************************************************

AULA 1

=>JavaScript é uma linguagem de programação popular usada para criar aplicativos interativos e dinâmicos para a web. Aqui estão alguns conceitos básicos de JavaScript:

=>Variáveis - Uma variável é um contêiner que armazena um valor. As variáveis em JavaScript são definidas usando a palavra-chave var, let ou const. 
Por exemplo, var nome = "João"; define uma variável chamada nome e atribui o valor "João" a ela.

=>Operadores - Os operadores em JavaScript são usados para realizar operações em variáveis e valores. Alguns dos operadores mais comuns incluem operadores aritméticos (+, -, *, /), operadores de comparação (>, <, >=, <=, ==, !=), operadores lógicos (&&, ||, !) e operadores de atribuição (=, +=, -=, *=, /=).
=> Condicionais - As declarações condicionais em JavaScript são usadas para executar um bloco de código com base em uma condição. As declarações condicionais incluem if, else if e else. 
Por exemplo, if (idade >= 18) { console.log("Você é maior de idade."); } else {console.log("Você é menor de idade."); } verifica se a idade é maior ou igual a 18 e exibe uma mensagem apropriada com base na condição.

=>Loops - Os loops em JavaScript são usados para executar um bloco de código várias vezes. Os loops incluem for, while e do...while. 
Por exemplo, for (var i = 0; i < 5; i++) { console.log(i); } exibe os números de 0 a 4 no console.

=>Funções - As funções em JavaScript são blocos de código que podem ser chamados várias vezes. As funções são definidas usando a palavra-chave function. 
Por exemplo, function saudacao(nome) { console.log("Olá, " + nome + "!"); } define uma função chamada saudacao que exibe uma saudação personalizada no console com base no nome passado como argumento.

Esses são apenas alguns dos conceitos básicos de JavaScript. Existem muitos outros recursos, como objetos, arrays, classes e eventos, que você pode aprender para se tornar um desenvolvedor proficientes em JavaScript.
********************************************************************************************************************************************************************************
=>node - Este comando é usado para executar um arquivo JavaScript no Node.js. Por exemplo, para executar um arquivo index.js, você pode digitar node index.js no terminal.
=>npm - Este é o gerenciador de pacotes do Node.js. Ele permite que você instale, atualize e remova pacotes e dependências do projeto. Alguns dos comandos mais comuns incluem:
-npm init - Inicializa um novo projeto do Node.js e cria um arquivo package.json para gerenciar as dependências do projeto.
-npm install - Instala todas as dependências listadas no arquivo package.json.
-npm install nome-da-dependencia - Instala uma dependência específica do projeto.
-npm uninstall nome-da-dependencia - Remove uma dependência específica do projeto.
-npm update - Atualiza todas as dependências para a versão mais recente.
-npm run nome-do-script - Executa um script personalizado definido no arquivo package.json.
=>fs - Este é o módulo do Node.js que fornece funções para trabalhar com o sistema de arquivos do computador. Alguns dos comandos mais comuns incluem:
-fs.readFileSync() - Lê um arquivo síncrono.
-fs.writeFile() - Escreve em um arquivo.
-fs.mkdirSync() - Cria um diretório.
-fs.readdirSync() - Lê um diretório.
=>http - Este é o módulo do Node.js que fornece funções para criar um servidor HTTP. Alguns dos comandos mais comuns incluem:
-http.createServer() - Cria um servidor HTTP.
-server.listen() - Inicia o servidor.
-server.on() - Manipula eventos no servidor.
=>express - Este é um framework web popular para Node.js que simplifica a criação de aplicativos web. Alguns dos comandos mais comuns incluem:
-express() - Cria um aplicativo Express.
-app.listen() - Inicia o servidor Express.
-app.get() - Define uma rota HTTP GET.
-app.post() - Define uma rota HTTP POST.
******************************************************************************************************************************************************************************
- Abra o terminal (no Windows, abra o Prompt de Comando ou PowerShell) e navegue até a pasta onde deseja criar o seu projeto.
- Execute o comando npm init e pressione Enter. Isso criará um novo arquivo package.json na pasta do seu projeto.
- Esse arquivo contém as informações do seu projeto e suas dependências.
- Escolha um nome para o seu projeto e preencha as informações solicitadas pelo comando npm init, como nome do autor, descrição do projeto, versão 
   inicial, entre outras.
-Agora, você pode instalar as dependências necessárias para o seu projeto usando o comando npm install nome-da-dependencia.
-Por exemplo, se você precisar instalar a biblioteca express, execute o comando npm install express e pressione Enter.
-Crie um novo arquivo de código-fonte em um editor de texto, como o Visual Studio Code, e salve-o com a extensão.js.
-Escreva o seu código JavaScript dentro do arquivo .js que você acabou de criar.
-Execute o arquivo .js usando o comando node nomedoarquivo.js e pressione Enter. Se o seu código estiver correto, você verá a saída no terminal.
******************************************************************************************************************************************************************************
 AULA 1_ NODE.Js 01/04/2023
******************************************************************************************************************************************************************************
const IUsers = require('./IUsers');
class Users extends IUsers{
 constructor(id=0,name='',password='',email=''){
    this.id= id;
    this.name= name;
    this.password= password;
    this.email= email;
 }
     getNameValue(){
      return this.name;
    }
     getPasswordValue(){     
            return this.password;
     }
     getIdValue(){
        return this.id;
     }
     getEmailValue(){
        return this.email;
     }
   setNameValue(name){
    this.name = name;
   }
  setEmailValue(email){
     this.email= email;
  }
   setPasswordValue(password){
    this.password= password;
   }
   setIdValue(id){
    this.id= id;
   }
    requiredValues(){
        if (this.id==0 || this.name=='' || this.email==''){
           throw new Error('Os Valores id, name e email sao obrigatorios');
        }
     return true;
    }
    isValidId(){
        if (this.id>0){
            return true;
        }
        return false;
    }
    isValidName(){
        var regexp = /^[a-zA-Z ]{2,50}$/;
         if (regexp.test(this.name)){
             return true;
         }
         return false;
    }
   isValidEmail(){
      var regexp =/^([a-zA-Z0-9\.-]+)@([a-z]+)\.([a-z]{2,8})(.[a-z]{2,8})?$/;
        if (regexp.test(this.email)){   
            return true;
        }
        return false;
   } 
 isValidPassword(){
    if (this.password.length>=6){
        return true;
    }
 return false;
}
}
###########################################################################################################################
 class IUsers{
 constructor(){
    if (new.target===IUsers){
    
###########################################################################################################################
const Users = require('./Users');
let users = new Users(1, 'Joao','joao@gmail.com' ,'123');
describe('Users', () => {
    it('should return true if the id is greater than 0', () => {
             expect(users.isValidId()).to.be.true;         
    });
    it('should return true if the name is valid', () => {       
        expect(users.isValidName()).to.be.true;
    });
    it('should return true if the email is valid', () => {
        expect(users.isValidEmail()).to.be.true;
    });
    it( 'should return true if password is greater equals than 6 characters', () => {
        expect(users.isValidPassword()).to.be.true;
    });
});
##########################################################################################################################
    module.exports = {
    testEnvironment: 'node',
    testMatch: ['**/*.spec.js'],
    testPathIgnorePatterns: ['/node_modules/'],
  };
##########################################################################################################################
   package.json
{
  "name": "exercicio1",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "jest"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "body-parser": "^1.20.2",
    "express": "^4.18.2",
    "jest": "^29.5.0"
  }
}
###########################################################################################################################
const Users = require('./Users');

describe('Users', () => {
   describe('id is valid',()=>{
    it('should return true if the id is greater than 0', () => {
            let users = new Users();
             users.setIdValue(1);
             expect(users.isValidId()).toBeTruthy();      
    });
 });
   describe('name is valid',()=>{
    it('should return true if the name is valid', () => {
        let users = new Users();
        users.setNameValue('edson');       
        expect(users.isValidName()).toBeTruthy();
    });
 });
 describe('email is valid',()=>{
 it('should return true if the email is valid', () => {
       let users = new Users();
       users.setEmailValue('edson@gmail.com');
        expect(users.isValidEmail()).toBeTruthy(); 
    });
});
describe('password is valid',()=>{
    it( 'should return true if password is greater equals than 6 characters', () => {
        let users = new Users();
        users.setPasswordValue('123456');
        expect(users.isValidPassword()).toBeTruthy(); 
    });
  });
});
###########################################################################################################################
const IUsers = require('./IUsers');

class Users extends IUsers {
    constructor(id = 0, name = '', password = '', email = '') {
        super();
        this.id = id;
        this.name = name;
        this.password = password;
        this.email = email;
    }
    getNameValue() {
        return this.name;
    }
    getPasswordValue() {
        return this.password;
    }
    getIdValue() {
        return this.id;
    }
    getEmailValue() {
        return this.email;
    }
    setNameValue(name) {
        this.name = name;
    }
    setEmailValue(email) {
        this.email = email;
    }
    setPasswordValue(password) {
        this.password = password;
    }
    setIdValue(id) {
        this.id = id;
    }

###########################################################################################################################
//CAMPOS OBRIGATORIOS
    requiredValues() {
        if (this.id == 0 || this.name == '' || this.email == '') {
            throw new Error('Os Valores id, name e email sao obrigatorios');
        }
        return true;
    }
//VALIDANDO OS CAMPOS
    isValidId() {
        if (this.id > 0) {
            return true;
        }
        return false;
    }
    //EXPRESSÃO REGULAR
    isValidName() {
        var regexp = /^[a-zA-Z ]{2,50}$/;
        if (regexp.test(this.name)) {
            return true;
        }
        return false;
    }
    // profedsonbelem23dfsdfsfsdfds @ gmail . com . br
    isValidEmail() {
        var regexp = /^([a-zA-Z0-9\.-]+)@([a-z]+)\.([a-z]{2,8})(.[a-z]{2,8})?$/;
        if (regexp.test(this.email)) {
            return true;
        }
        return false;
    }
    isValidPassword() {
        if (this.password.length >= 6) {
            return true;
        }
        return false;
    }
}
module.exports = Users;
###########################################################################################################################
const users = require('./Users.model');
let listUsers =[{ 
  id:1,
  name:'edson',
  password:'123456',
  email:'edson@gmail.com'
},
{
    id:2,
    name:'luciana',
    password:'123456',
    email:'luciana@gmail.com',
},
{
    id:3,
    name:'carlos',
    password:'123456',
    email:'carlos@gmail.com',
}
];
module.exports=listUsers;
###########################################################################################################################
package br.com.arq.interfaces;

public interface IBook {

	public void setIdBook(Integer idBook);
	public Integer getIdBook();
	
	public void setName(String name);
	public String getName();
	
	public void setDescription(String description);
	public String getDescription();
	
	public void setPrice(Double price);
	public Double getPrice();
	
	//CTRL + S - para salvar
}
###########################################################################################################################
package br.com.arq.entity;

import br.com.arq.interfaces.IBook;

public class Book implements IBook {

	private Integer idBook;

	private String name;

	private String description;

	private Double price;

	public Integer getIdBook() {
		return idBook;
	}

	public void setIdBook(Integer idBook) {
		this.idBook = idBook;
	}

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}

	public String getDescription() {
		return description;
	}

	public void setDescription(String description) {
		this.description = description;
	}

	public Double getPrice() {
		return price;
	}

	public void setPrice(Double price) {
		this.price = price;
	}
}
____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
> CURIOSIDADES PROPRIAS: Java//
  Para nao esquecer : 
- Tudo que esta com "/////////" significa que posso modificar. 
- Se eu tirar a linha 27, fica normal porque posso colocar o nome que eu quiser ou seja gravar somente o CODIGO base que vou colocar no ultimo bloco.
- Se alterar o String, tenho que mudar no final LINHA 27, para ter o resultado. (CASO USE A LINHA 27 para baixo).
- Se alterar o  (((((((((String nome = sc.nextLine(); ))))))))) para ((((((((String apelido = sc.nextLine();)))))))))))))) funciona igualmente.
-  Int ////// = sc.nextInt(); =>  Sempre para números, (confirmar ainda). 
- Se retirar a linha 27 para baixo, funciona normalmente, porem sem gerar o ("cliente: nome") em diante.
- Posso alterar as frases não alteram o questionario gerado.
___________________________________________________________________________________________________________________________
                                                                                 JAVA  => CODIGO PARA BASE DE OUTROS.

public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("//////////////////////////////////////////");

        System.out.print("///////////////////////////////////////////////");
        String ///////////////// = sc.nextLine();

        System.out.print("//////////////////////////////////////////");
        int ////////// = sc.nextInt(); ---------->Codigo para (numeros, idades)

        sc.nextLine(/////////////////////////////////); 

        System.out.print("//////////////////////////");
        String ////////////// = sc.nextLine();

        System.out.print("/////////////////////////////");
        String ///////////////////// = sc.nextLine();

        System.out.println("\n/////////////////////////////////////");

        System.out.println("////////: " + //////////////);
        System.out.println("/////////: " + //////////////);
        System.out.println("//////////: " + /////////////);
        System.out.println("///////////: " + /////////////////);
    }
}
______________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
                                                                                                 GRAVANDO DADOS 
import java.io.FileWriter;
import java.io.PrintWriter;
import java.security.MessageDigest;
import java.security.NoSuchAlgorithmException;
import java.util.Scanner;

public class GravadorDeDados {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Digite o seu nome:");
        String nome = input.nextLine();
        System.out.println("Digite o seu telefone:");
        String telefone = input.nextLine();
        System.out.println("Digite o seu e-mail:");
        String email = input.nextLine();
        System.out.println("Digite a sua senha:");
        String senha = input.nextLine();

        // Criptografa a senha usando o algoritmo SHA-256
        String senhaCriptografada = criptografarSenha(senha);

        // Grava os dados no arquivo "dados.txt"
        try {
            FileWriter arquivo = new FileWriter("dados.txt", true);
            PrintWriter gravador = new PrintWriter(arquivo);
            gravador.println(nome + ";" + telefone + ";" + email + ";" + senhaCriptografada);
            gravador.close();
            System.out.println("Dados gravados com sucesso!");
        } catch (Exception e) {
            System.out.println("Erro ao gravar os dados no arquivo.");
        }
    }

    public static String criptografarSenha(String senha) {
        try {
            MessageDigest md = MessageDigest.getInstance("SHA-256");
            byte[] hash = md.digest(senha.getBytes());
            StringBuilder sb = new StringBuilder();
            for (byte b : hash) {
                sb.append(String.format("%02x", b));
            }
            return sb.toString();
        } catch (NoSuchAlgorithmException e) {
            System.out.println("Erro ao criptografar a senha.");
            return null;
        }
    }
}
_________________________________________________________________________________________________________________________
                                                                                             CODIGO  ORIGINAL

public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Por favor, responda algumas perguntas sobre você:");

        System.out.print("Qual é o seu nome completo? ");
        String nome = sc.nextLine();

        System.out.print("Qual é a sua idade? ");
        int idade = sc.nextInt();

        sc.nextLine(); // Consumir a nova linha pendente

        System.out.print("Qual é o seu endereço de e-mail? ");
        String email = sc.nextLine();

        System.out.print("Qual é o seu gênero? ");
        String genero = sc.nextLine();

        System.out.println("\nObrigado por responder! Aqui estão suas respostas:");

        System.out.println("Nome: " + nome);
        System.out.println("Idade: " + idade);
        System.out.println("E-mail: " + email);
        System.out.println("Gênero: " + genero);
    }
}
__________________________________________________________________________________________________________________________
                                                                      COMO CRIAR UM REPOSITORIO NO GITHUB? 
- Download do git na maquina.
- abrir o terminal git bash 
- primeira vez usando git com conta nova deve ser configurado 
- colocando meu nome meu email, que sera para onde meus proojetos irao
- comandos para essa configuracao
* $ git config --global user.name "Nome do usuário"
* $ git config --global user.email "seu@email.com"
- devo saber em que pasta coloquei meu projeto antes de subir ele 
- O comando ls indica a pasta que esta meu desktop com meu projeto
- cd Desktop diz qual  meu objeto na pasta
__________________________________________________________________________________________________________________________
                                                                    CLONANDO PROJETOS ( GITHUB )
- abro github
- abro o projeto que quero pegar.
- clico no botao verde do canto superior direito 
- copio a url que esta a mostra
- abro git bash
- acesso a pasta desktop com o codigo ( cd Desktop ) dou enter e vai abrir outra sequencia. 
- coloco  ( git clone) e colo o url que copiei  
- vai gerar uma mensagem/codigo dizendo se foi bem sucedido ou nao
- depois de clonado verificar se esta na pasta que escolhi e se existe ( ls )  
- entro no repositorio clonado e vejo se a branch mostra os arquivos que existem no projeto clonado ( cd nome_do_repositorio:)
- olho historico de commits com o comando ( git log) 
- com o comando (git log --oneline)  vejo se mostrara informacoes do commit de forma mais resumida
-  Link de todo passo a passo detalhado:
 https://www.alura.com.br/artigos/clonando-repositorio-git-github?gclid=Cj0KCQjw8e-gBhD0ARIsAJiDsaU12aTocD8Ni7ez44RATunhR8h428XEtQwBA3cVJO8WNNwmN2nZjDEaAv_bEALw_wcB

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
JA USADOS

import java.util.Scanner;

public class PedidoDequalquercoisa {

           public static void main(String[] args) throws InterruptedException {
	        Scanner scanner = new Scanner(System.in);

	        System.out.println("Olá, qual é o seu nome?");
	        String nome = scanner.nextLine();

	        System.out.println("O meu é pamela.");
	        System.out.println("Eu queria te fazer uma pergunta muito importante..." + nome + "!");

	        for (int i = 5; i > 0; i--) {
	            System.out.println(i);
	            Thread.sleep(1000);
	        }

	        System.out.println("Você me desculpa " + nome + "?");
	        String resposta = scanner.nextLine();

	        if (resposta.equalsIgnoreCase.("sim")) {
	            System.out.println("Que ótimo! Eu te Amo muito!");
	        } else {
	            System.out.println("Tudo bem, obrigado pela sua resposta.");

	  if (resposta("nao")) {
	            System.out.println("tudo bem.");
	         }
	  
	
}


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------




         public class Teste {
	
	public static void main (final String[] args) {
		
		
		System.out.println("3 motivos porque eu te amo:");
		
		Pessoa p1 = new Pessoa();
		p1.nome = "Voce é a pessoa mais determinada";
		System.out.println(Pessoa.contador + " -> " + p1.nome );
		
		Pessoa p2 = new Pessoa();
		p2.nome = "BBBB";
		System.out.println(Pessoa.contador + " -> " + p2.nome );
	}

}



--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    



        public class Pessoa {
	
	static int contador;
	String nome;
	
	public Pessoa() {
		contador++;
	}

}

