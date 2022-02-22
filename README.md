# -EntradaBlog-Iniciales
 EntradaBlog+Iniciales
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package entradablog.iniciales;

/**
 *
 * @author Ana
 */
/*Clase para manejar las entradas de un blog.
 * La clase se creó el 21/3/1999 por Ana.
 * Esta es la versión 2.3
 */
//Modificar.

public class EntradaBlogIniciales {
/**
 * 
 */
	public static char separador=':';
	private int id;
	private String texto;
	private String autor;
	/**
         * 
         * @param Ana
         * @throws IllegalArgumentException 
         */
	//Constructor de la clase. recibe el número de entrada, el nombre del autor
	//de la entrada y el texto que contiene la entrada. Si el número de entrada
	//es negativo, lanza una excepción.
	public EntradaBlogIniciales(String autor)throws IllegalArgumentException{
		if(id<=0){
                    throw new IllegalArgumentException("El id no puede ser negativo");
                }
		this.id=id;
		this.autor=autor;
		this.texto=texto;
	}
        /**
         * 
         * @return 
         */
	@Override
	public String toString(){
		String cad="";
		cad+="\nENTRADA DE"+separador+autor;
		cad+="\n "+texto;
		return cad;
	}
	
	//Devuelve el número de la entrada
       
	public int getId(){
		return this.id;
	}
	
	//devuelve el texto completo de la entrada
	public String getTexto(){
		return this.texto;
	}
	
	//devuelve el nombre del autor de la entrada en mayúsculas
	public String getAutor(){
		return this.autor.toUpperCase();
	}
	
	//devuelve el nombre del autor. Ya no se usa. Mejor ver getAutor
	public String devuelveAutor(){
		return this.autor;
	}
	
	//No tiene porqué tener argumentos.
	public static void main(String[] args) {
                //Modificar.
		EntradaBlogIniciales e1=new EntradaBlogIniciales ("-3" + "ana" + "Últimas noticias, está disponible BixBy 2.0");
		System.out.println(e1);
	}
}
