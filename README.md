# SC-900-Microsoft-Security-Compliance-and-Identity-Fundamentals
Notas para este examen


# The shared responsibility model

The shared responsibility model identifies which security tasks are handled by the cloud provider, and which security tasks are handled by you, the customer. The responsibilities vary depending on where the workload is hosted:


Centros de datos locales . En un centro de datos local, tiene la responsabilidad de todo, desde la seguridad física hasta el cifrado de datos confidenciales.

## Infraestructura como servicio (IaaS)

De todos los servicios en la nube, IaaS requiere la mayor gestión por parte del cliente de la nube. Con IaaS, está utilizando la infraestructura informática del proveedor de la nube. El cliente de la nube no es responsable de los componentes físicos, como las computadoras, la red o la seguridad física del centro de datos. Sin embargo, el cliente de la nube aún tiene la responsabilidad de los componentes de software, como los sistemas operativos, los controles de red, las aplicaciones y la protección de datos.

## Plataforma como Servicio (PaaS) 

PaaS proporciona un entorno para crear, probar e implementar aplicaciones de software. El objetivo de PaaS es ayudarlo a crear una aplicación rápidamente sin administrar la infraestructura subyacente. Con PaaS, el proveedor de la nube administra el hardware y los sistemas operativos, y el cliente es responsable de las aplicaciones y los datos.

## Software como servicio (SaaS) 

SaaS está alojado y administrado por el proveedor de la nube, para el cliente. Por lo general, se licencia a través de una suscripción mensual o anual. Microsoft 365, Skype y Dynamics CRM Online son ejemplos de software SaaS. SaaS requiere la menor cantidad de administración por parte del cliente de la nube. El proveedor de la nube es responsable de administrar todo, excepto los datos, los dispositivos, las cuentas y las identidades.

# Describe defense in depth

Defense in depth uses a layered approach to security, rather than relying on a single perimeter. A defense in-depth strategy uses a series of mechanisms to slow the advance of an attack. Each layer provides protection so that, if one layer is breached, a subsequent layer will prevent an attacker getting unauthorized access to data.


![4-defense-depth](https://user-images.githubusercontent.com/63270579/194113325-e678394b-85f9-41e7-b289-d42c83d494ac.png)

Example layers of security might include:


## Physical securit
y such as limiting access to a datacenter to only authorized personnel.

## Identity and access
security controls, such as multifactor authentication or condition-based access, to control access to infrastructure and change control.

## Perimeter 
security of your corporate network includes distributed denial of service (DDoS) protection to filter large-scale attacks before they can cause a denial of service for users.

## Network 
security
such as network segmentation and network access controls, to limit communication between resources.

## Compute
layer security such as securing access to virtual machines either on-premises or in the cloud by closing certain ports.

## Application
layer security to ensure applications are secure and free of security vulnerabilities.

## Data
layer security including controls to manage access to business and customer data and encryption to protect data.















