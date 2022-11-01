# Leitura-cria-o-e-escritura-de-arquivo-java

package manipulararquivo;

import java.io.File;
import java.io.FileWriter;
import java.io.FileReader;
import java.io.IOException;
import java.util.Scanner;

public class Arquivos {
    public static void createFile(String path){
        try{
            File arq = new File(path);
            if(arq.createNewFile()){
                System.out.println("arquivo criado"+arq.getName());
            }else{
                System.out.println("Erro ao criar arquivo");
            }
            
        }catch(Exception e){
            System.out.println("Erro!!");
        }
    }
    
    public static void writeFile(String path, String texto){
        try{
            
            FileWriter arq = new FileWriter(path);
            arq.write(texto);
            arq.close(); 
            
        }catch(Exception e){
            System.out.println("Erro!");
        }
        
        ----------------------------------------------------------------
        
        package manipulararquivo;
public class ManipularArquivo {
    public static void main(String[] args) {
        String path = "file2.txt";
        String texto = "Vai Corinthians";
        Arquivos arq = new Arquivos();
        
        arq.createFile(path);
        arq.writeFile(path, texto);
        arq.readerFile(path);
    }
    
}
    }
       
    public static void readerFile(String path){
    
    try{
        
        FileReader arq = new FileReader(path);
        Scanner scr = new Scanner(arq);
        
        while(scr.hasNextLine()){
            String linha = scr.nextLine();
            System.out.println(linha);
        }
        
    }catch(Exception e){
        System.out.println("erro!");
    }
    
}
   
}
