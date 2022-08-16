# aasaa
progra
import java.io.* ;

public class Testread {

	public static void main(String[] args) throws IOException {
		
		BufferedReader usuario = new BufferedReader( new InputStreamReader( System.in ) );
		
		//datos fijos
		String dato;
		int i=0;
		int largo=1000 , opcion;
		long SumaEdades=0;
		double promedio;
		
		//datos dynamicos
		String[] nombres;nombres= new String[largo];
		int[] edad;edad= new int[largo];
		long[] telefono;telefono= new long[largo];
		
		while(true) {
			System.out.print("MENU\n"
			+ "	1.-AGREGAR\n"
			+ "	2.-LISTAR\n"
			+ "	3.-BUSCAR\\n"
			+ "	4.-SALIR\\n");
			
			System.out.print("	Ingrese la Opcion: ");
			dato = usuario.readLine( ) ;
			nombres[i] = dato;
			
			//ingreso
			for(i=0;i<largo;i++) {
				
				System.out.print("Persona:"+(i+1)+"\n");
				
				System.out.print("	Ingrese el nombre: ");
				dato = usuario.readLine( ) ;
				nombres[i] = dato;
				
				System.out.print("	Ingrese la edad: ");
				dato = usuario.readLine( ) ;
				edad[i] = Integer.parseInt( dato );
				
				SumaEdades+=edad[i];
				
				System.out.print("	Ingrese el telefono: ");
				dato = usuario.readLine( ) ;
				telefono[i] = Integer.parseInt( dato );
				
				System.out.print("Datos ingresados como \n"
						+"	[Nombre:"+nombres[i]+"]\n"
						+"	[Edad:"+edad[i]+"]\n"
						+"	[Fono:"+telefono[i]+"]\n");
			
		}
		
		
		promedio=(double) SumaEdades/largo;
		System.out.println("Promedio de edades es :"+promedio);
		}
		
	}

}
