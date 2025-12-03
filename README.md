# 🏥 Sistema de Gestión Hospitalaria

## 📘 Descripción General
El **Sistema de Gestión Hospitalaria** es una aplicación desarrollada para optimizar el manejo de pacientes, personal médico y procesos internos de un hospital. Está diseñado para mejorar la eficiencia del registro, consulta y administración de información crítica, integrando módulos de gestión y una conexión segura con una base de datos MySQL.

Este sistema fue desarrollado en **Java (NetBeans 8.2)** utilizando el patrón MVC y conexión directa mediante clases personalizadas.

---

## 🎯 Objetivos del Proyecto

- Facilitar la gestión de pacientes, personal médico y administrativo mediante una interfaz intuitiva.
- Garantizar un acceso rápido y seguro a los registros hospitalarios.
- Integrar un módulo de conexión a MySQL mediante clases dedicadas para consultas, inserciones y actualizaciones.
- Optimizar los procesos de admisión, seguimiento clínico y organización interna.

---

## 📍 Alcance del Sistema

El sistema abarca las siguientes funcionalidades principales:

- Registro y gestión de pacientes.
- Administración del personal hospitalario.
- Consulta y actualización de historiales.
- Gestión de turnos y procesos internos.
- Conexión con base de datos MySQL para almacenar y consultar información.

Este proyecto es escalable y permite la incorporación de módulos adicionales según las necesidades del hospital.

---

## ⚙️ Funcionalidades Principales

### 🧑‍⚕️ Gestión de Pacientes
- Registro de nuevos pacientes.
- Consulta de historial clínico.
- Actualización de datos.

### 👨‍⚕️ Gestión del Personal
- Registro de médicos y personal administrativo.
- Asignación de roles y turnos.

### 📑 Procesos Hospitalarios
- Control de citas.
- Administración interna de módulos complementarios.

### 🗄 Conexión a Base de Datos
El sistema cuenta con clases específicas:

#### **🔹 ConexionBD.java**
Clase encargada de establecer la conexión con MySQL.  
Implementación realizada para el requerimiento **PSGH-4**, donde se generó la clase y se configuró la conexión.

#### **🔹 Metodos_SQL.java**
Clase que contiene los métodos de consulta, inserción, actualización y eliminación de datos.

---

## 🛠 Tecnologías Utilizadas

### **Lenguaje**
- Java

### **IDE**
- NetBeans 8.2

### **Base de Datos**
- MySQL

### **Arquitectura**
- MVC (Modelo - Vista - Controlador)

---

# 🚀 Instalación y Configuración

## 🟦 1. Clonar el repositorio

```bash
git clone https://github.com/usuario/sistema-hospital.git
```

---

## 🟦 2. Configurar la base de datos MySQL

Abrir **phpMyAdmin** o tu cliente MySQL preferido.

### 📌 Crear la base de datos:

```sql
CREATE DATABASE hospital_db;
```

### 📌 Importar el archivo SQL (si existe):

```
/database/hospital.sql
```

---

## 🟦 3. Configurar la conexión en Java

Editar **ConexionBD.java**:

```java
public class ConexionBD {
    Connection conectar = null;

    public Connection conexion() {
        try {
            Class.forName("com.mysql.jdbc.Driver");
            conectar = DriverManager.getConnection("jdbc:mysql://localhost/hospital_db", "root", "");
            System.out.println("Conexión exitosa");
        } catch (Exception e) {
            System.out.println("Error al conectar: " + e.getMessage());
        }
        return conectar;
    }
}
```

---

# 📁 Estructura del Proyecto (Referencial)

```bash
/src
├── controllers
├── models
├── views
└── database
    ├── ConexionBD.java
    └── Metodos_SQL.java
```

---

# 👥 Colaboradores

| Nombre            | Rol          |
|------------------|--------------|
| Fernando Sánchez | Desarrollador |
| Marlon Copara    | Desarrollador |
| Enrique Ortiz    | Desarrollador |

---

# 🔮 Mejoras Futuras

- Módulo de hospitalización  
- Gestión de farmacia  
- Panel administrativo avanzado  
- Reportes automáticos  
- Integración con sistemas externos



