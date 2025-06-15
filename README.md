using System;

namespace RegistroEstudiante
{
    // Clase que representa un estudiante
    public class Estudiante
    {
        // Atributos del estudiante
        public int Id;
        public string Nombres;
        public string Apellidos;
        public string Direccion;
        public string[] Telefonos;

        // Constructor
        public Estudiante(int id, string nombres, string apellidos, string direccion, string[] telefonos)
        {
            Id = id;
            Nombres = nombres;
            Apellidos = apellidos;
            Direccion = direccion;
            Telefonos = telefonos;
        }

        // Método para mostrar información del estudiante
        public void MostrarInformacion()
        {
            Console.WriteLine("ID: " + Id);
            Console.WriteLine("Nombres: " + Nombres);
            Console.WriteLine("Apellidos: " + Apellidos);
            Console.WriteLine("Dirección: " + Direccion);
            Console.WriteLine("Teléfonos:");
            for (int i = 0; i < Telefonos.Length; i++)
            {
                Console.WriteLine($"  Teléfono {i + 1}: {Telefonos[i]}");
            }
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // Datos simulados para el estudiante
            string[] telefonos = new string[3] { "0987654321", "0998765432", "0976543210" };

            // Crear una instancia de estudiante
            Estudiante estudiante = new Estudiante(
                1,
                "Juan",
                "Pérez Martínez",
                "Av. Siempre Viva 123",
                telefonos
            );

            // Mostrar información
            estudiante.MostrarInformacion();
        }
    }
}

