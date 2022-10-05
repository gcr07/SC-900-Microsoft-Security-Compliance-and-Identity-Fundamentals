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


# La Triada de la ciberseguridad Confidentiality, Integrity, Availability (CIA)

## Confidentiality 

refers to the need to keep confidential sensitive data such as customer information, passwords, or financial data. You can encrypt data to keep it confidential, but then you also need to keep the encryption keys confidential. Confidentiality is the most visible part of security; we can clearly see need for sensitive data, keys, passwords, and other secrets to be kept confidential.

## Integrity 

refers to keeping data or messages correct. When you send an email message, you want to be sure that the message received is the same as the message you sent. When you store data in a database, you want to be sure that the data you retrieve is the same as the data you stored. Encrypting data keeps it confidential, but you must then be able to decrypt it so that it's the same as before it was encrypted. Integrity is about having confidence that data hasn't been tampered with or altered.

## Availability 

refers to making data available to those who need it, when they need it. It's important to the organization to keep customer data secure, but at the same time it must also be available to employees who deal with customers. While it might be more secure to store the data in an encrypted format, employees need access to decrypted data.

While the goals of a cybersecurity strategy are to preserve the confidentiality, integrity, and availability of systems, networks, applications, and data; it's the goal of cybercriminals to disrupt these goals. Microsoft’s portfolio includes the solutions and technologies to enable organizations to deliver on the goals of the CIA triad.

# Describe the Zero Trust model ( da por sentado que la red fue vulnerada )

Zero Trust assumes everything is on an open and untrusted network, even resources behind the firewalls of the corporate network. The Zero Trust model operates on the principle of “trust no one, verify everything.”


# Zero Trust guiding principles ( el que siempre olvidas and assume breach)

The Zero Trust model has three principles which guide and underpin how security is implemented. These are: verify explicitly, least privilege access, and assume breach.

## Verify explicitly.

Always authenticate and authorize based on the available data points, including user identity, location, device, service or workload, data classification, and anomalies.

## Least privileged access.  # (JIT/JEA) que te encontraste en el otro examen y no supiste) 

Limit user access with just-in-time and just-enough access (JIT/JEA), risk-based adaptive policies, and data protection to protect both data and productivity.

## Assume breach

Segment access by network, user, devices, and application. Use encryption to protect data, and use analytics to get visibility, detect threats, and improve your security.








