// Tarea_semana_13

// Desarrolle un traductor básico de inglés español o español ingles.

using System; // Importa el espacio de nombres System, que contiene clases básicas como Console.
using System.Collections.Generic; // Importa el espacio de nombres Collections.Generic, que contiene clases como List.

class RevistaCatalogo
{
    private List<string> catalogo; // Declara una lista privada para almacenar los títulos de las revistas.

    public RevistaCatalogo()
    {
        catalogo = new List<string>(); // Inicializa la lista de títulos de revistas.
    }

    public void AgregarTitulo(string titulo)
    {
        catalogo.Add(titulo); // Agrega un título a la lista de revistas.
    }

    public string BuscarTitulo(string titulo)
    {
        return BuscarTituloRecursivo(titulo, 0) ? "encontrado" : "no encontrado"; // Llama al método recursivo para buscar el título y devuelve "encontrado" o "no encontrado".
    }

    private bool BuscarTituloRecursivo(string titulo, int indice)
    {
        if (indice >= catalogo.Count) // Verifica si el índice ha superado el tamaño de la lista.
            return false; // Si es así, devuelve false.
        if (catalogo[indice].Equals(titulo, StringComparison.OrdinalIgnoreCase)) // Compara el título en el índice actual con el título buscado, ignorando mayúsculas y minúsculas.
            return true; // Si son iguales, devuelve true.
        return BuscarTituloRecursivo(titulo, indice + 1); // Llama recursivamente al método con el siguiente índice.
    }

    public void MostrarMenu()
    {
        Console.WriteLine("Menu:"); // Muestra el menú.
        Console.WriteLine("1. Buscar un titulo"); // Opción para buscar un título.
        Console.WriteLine("2. Salir"); // Opción para salir.
    }
}

class Program
{
    static void Main()
    {
        RevistaCatalogo catalogo = new RevistaCatalogo(); // Crea una instancia de RevistaCatalogo.
        catalogo.AgregarTitulo("Vistazo"); // Agrega títulos de revistas ecuatorianas.
        catalogo.AgregarTitulo("Hogar"); 
        catalogo.AgregarTitulo("Ecuador Inmediato");
        catalogo.AgregarTitulo("Revista Mundo Diners");
        catalogo.AgregarTitulo("Revista Gestión");
        catalogo.AgregarTitulo("Revista Ñan");
        catalogo.AgregarTitulo("Revista Soho Ecuador");
        catalogo.AgregarTitulo("Revista Clave");
        catalogo.AgregarTitulo("Revista Ekos");
        catalogo.AgregarTitulo("Revista América Economía");

        while (true) // Bucle infinito para mostrar el menú hasta que el usuario decida salir.
        {
            catalogo.MostrarMenu(); // Muestra el menú.
            Console.Write("Seleccione una opcion: "); // Solicita al usuario que seleccione una opción.
            int opcion = int.Parse(Console.ReadLine()); // Lee la opción seleccionada por el usuario.

            if (opcion == 1) // Si la opción es 1, busca un título.
            {
                Console.Write("Ingrese el título a buscar: "); // Solicita el título a buscar.
                string titulo = Console.ReadLine(); // Lee el título ingresado por el usuario.
                Console.WriteLine(catalogo.BuscarTitulo(titulo)); // Muestra el resultado de la búsqueda.
            }
            else if (opcion == 2) // Si la opción es 2, sale del bucle.
            {
                break; // Rompe el bucle y termina el programa.
            }
            else // Si la opción no es válida, muestra un mensaje de error.
            {
                Console.WriteLine("Opción no válida. Intente de nuevo."); // Mensaje de opción no válida.
            }
        }
    }
}

// Fin del programa.

// Universidad Estatal Amazónica.

// Andrés Ponce M.