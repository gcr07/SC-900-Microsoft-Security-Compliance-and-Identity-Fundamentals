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

# Six foundational pillars

In the Zero Trust model, all elements work together to provide end-to-end security. These six elements are the foundational pillars of the Zero Trust model:

## Identities
may be users, services, or devices. When an identity attempts to access a resource, it must be verified with strong authentication, and follow least privilege access principles.

## Devices
create a large attack surface as data flows from devices to on-premises workloads and the cloud. Monitoring devices for health and compliance is an important aspect of security.

## Applications 
are the way that data is consumed. This includes discovering all applications being used, sometimes called Shadow IT because not all applications are managed centrally. This pillar also includes managing permissions and access.

## Data
should be classified, labeled, and encrypted based on its attributes. Security efforts are ultimately about protecting data, and ensuring it remains safe when it leaves devices, applications, infrastructure, and networks that the organization controls.

## Infrastructure
, whether on-premises or cloud based, represents a threat vector. To improve security, you assess for version, configuration, and JIT access, and use telemetry to detect attacks and anomalies. This allows you to automatically block or flag risky behavior and take protective actions.

## Networks 
should be segmented, including deeper in-network micro segmentation. Also, real-time threat protection, end-to-end encryption, monitoring, and analytics should be employed.

## Trabajando todo el Zero trust Model en conjunto con sus 6 pilares y 3 princios

![2-zero-trust-pillars-v2](https://user-images.githubusercontent.com/63270579/194115915-59e5d772-09af-49a9-b056-0adba9f7e2be.png)

# Describe encryption and hashing

![6-encryption](https://user-images.githubusercontent.com/63270579/194116571-1cd2dc93-303b-4901-bc33-f5cd917c0fad.png)
Ya te sabes esta parte.

El esquema asimétrico resuelve el problema de necesitar una clave pre-establecida. Se divide la clave en dos partes par de claves): la clave pública y la clave privada. Dichas claves son complementarias: Un mensaje encriptado con la clave pública sólo puede ser desencriptado con la correspondiente clave privada. Por lo tanto, el conocimiento de la clave pública no implica capacidad de desencriptación. Así, una persona podrá difundir su clave pública para que cualquiera pueda enviarle un mensaje cifrado que solamente podrá desencriptarse con la clave privada. ***Mesaje encritpado con clave publica solo puede see desencriptado con la clave privada***.

## Encryption for data at rest

Data at rest is the data that's stored on a physical device, such as a server. It may be stored in a database or a storage account but, regardless of where it's stored, encryption of data at rest ensures the data is unreadable without the keys and secrets needed to decrypt it.

If an attacker obtained a hard drive with encrypted data and didn't have access to the encryption keys, they would be unable to read the data.

## Encryption for data in transit

Data in transit is the data moving from one location to another, such as across the internet or through a private network. Secure transfer can be handled by several different layers. It could be done by encrypting the data at the application layer before sending it over a network. HTTPS is an example of encryption in transit.

Encrypting data in transit protects it from outside observers and provides a mechanism to transmit data while limiting the risk of exposure.

## Encryption for data in use

A common use case for encryption of data in use involves securing data in nonpersistent storage, such as RAM or CPU caches. This can be achieved through technologies that create an enclave (think of this as a secured lockbox) that protects the data and keeps data encrypted while the CPU processes the data.


# Hashing

Ya te la sabes

Hashing uses an algorithm to convert text to a unique fixed-length value called a hash. Each time the same text is hashed using the same algorithm, the same hash value is produced. That hash can then be used as a unique identifier of its associated data.


# Describe compliance concepts

Esto trata de como se potegen los datos y conceptos de cumplimiento(por ejemplo en francia no se pueden sacar los datos de ese pais de los usuarios todo debe de estar guardado en servidores que esten dentreo de Francia).

Government agencies and industry groups have issued regulations to help protect and govern the use of data. From personal and financial information to data protection and privacy, organizations can be accountable for meeting dozens of regulations to be compliant. Listed below are some important concepts and terms that relate to data compliance.

## Conceptos Generales importantes ( definidos pro azure en su material de lectura)

## Data residency -

When it comes to compliance, data residency regulations govern the physical locations where data can be stored and how and when it can be transferred, processed, or accessed internationally. These regulations can differ significantly depending on jurisdiction.

## Data sovereignty 

- Another important consideration is data sovereignty, the concept that data, particularly personal data, is subject to the laws and regulations of the country/region in which it's physically collected, held, or processed. This can add a layer of complexity when it comes to compliance because the same piece of data can be collected in one location, stored in another, and processed in still another; making it subject to laws from different countries/regions.

## Data privacy - 

Providing notice and being transparent about the collection, processing, use, and sharing of personal data are fundamental principles of privacy laws and regulations. Personal data means any information relating to an identified or identifiable natural person. Privacy laws previously referenced "PII" or "personally identifiable information" but the laws have expanded the definition to any data that is directly linked or indirectly linkable back to a person. Organizations are subject to, and must operate consistent with, a multitude of laws, regulations, codes of conduct, industry-specific standards, and compliance standards governing data privacy.


# Identidad

![3-identity-new-security-perimeter](https://user-images.githubusercontent.com/63270579/194121349-78002b7c-430e-481a-b00c-0e832a594556.png)


Todos los usuarios y todos los dispositivos tienen una identidad que se puede usar para tener acceso a los recursos. La identidad es la forma en que se identifican las personas y las cosas en la red corporativa y en la nube. Tener la seguridad de quién o qué está accediendo a los datos de la organización y otros recursos es una parte fundamental de la protección del entorno.

## Atenticacion y Autorizacion 

Supongamos que quiere pasar la noche en un hotel. Lo primero que hará es ir a la recepción para iniciar el "proceso de autenticación". Una vez que el recepcionista haya comprobado quién es, le dará una tarjeta-llave y ya podrá dirigirse a su habitación. Piense en la tarjeta-llave como el proceso de autorización. La tarjeta-llave solo le permitirá abrir las puertas y los ascensores a los que puede acceder, como la puerta de su habitación.

En términos de ciberseguridad, la autorización determina el nivel de acceso o los permisos de una persona autenticada a los datos y los recursos. A veces, la autorización se abrevia como AuthZ.

Acronimo que me parecio interesante BYOD o Bring Your Own Device

El modelo de seguridad tradicional basado en el perímetro ya no es suficiente. La identidad se ha convertido en el nuevo perímetro de seguridad que permite a las organizaciones proteger sus recursos.

Pero ¿qué significa una identidad? Una identidad es el conjunto de aspectos que definen o caracterizan a alguien o algo. Por ejemplo, la identidad de una persona incluye la información que usa para autenticarse, como su nombre de usuario y contraseña, y su nivel de autorización.

Una identidad puede estar asociada a un usuario, una aplicación, un dispositivo o cualquier otra cosa.

## Cuatro pilares de una infraestructura de identidad

La identidad es un concepto que abarca todo un entorno, por lo que las organizaciones deben pensar en ello en general. Hay una colección de procesos, tecnologías y directivas para administrar identidades digitales y controlar cómo se usan para tener acceso a los recursos. Pueden organizarse en cuatro pilares fundamentales que las organizaciones deben tener en cuenta al crear una infraestructura de identidad.

### Administración.

La administración consiste en la creación y la administración o gobernanza de identidades para los usuarios, dispositivos y servicios. Como administrador, puede administrar cómo y en qué circunstancias pueden cambiar las características de las identidades (se pueden crear, actualizar y eliminar).

### Autenticación. 

El pilar de autenticación indica cuánto necesita saber un sistema de TI sobre una identidad para tener pruebas suficientes de que realmente son quienes dicen ser. Implica el acto de solicitar a un usuario credenciales legítimas.

## Autorización.

El pilar de autorización trata sobre el procesamiento de los datos de identidad entrante para determinar el nivel de acceso de una persona o servicio autenticado dentro de la aplicación o servicio al que quiere obtener acceso.

## Auditoría

El pilar de auditoría consiste en realizar un seguimiento de quién realiza qué, cuándo, dónde y cómo. La auditoría incluye la creación de informes, alertas y gobernanza de identidades en profundidad.

Direccionar cada uno de estos cuatro pilares es clave para una solución completa y sólida de identidad y control de acceso.

# Descripción del rol del proveedor de identidades

![Modern Autentication ](https://user-images.githubusercontent.com/63270579/194124731-accb021e-5ec6-4685-a45e-e972a7969b1f.PNG)

Autenticación moderna es un término genérico para los métodos de autenticación y autorización entre un cliente, como un portátil o un teléfono, y un servidor, como un sitio web o una aplicación. ***En el centro de la autenticación moderna está el rol del proveedor de identidades. Un proveedor de identidades crea, mantiene y administra la información de identidad al tiempo que proporciona servicios de autenticación, autorización y auditoría.***

Con la autenticación moderna, quien proporciona todos los servicios, incluidos todos los servicios de autenticación, es un proveedor de identidades central. El proveedor de identidades almacena y administra de forma centralizada la información que se usa para autenticar el usuario en el servidor.

Con un proveedor de identidades central, las organizaciones pueden establecer directivas de autenticación y autorización, supervisar el comportamiento de los usuarios, identificar actividades sospechosas y reducir los ataques malintencionados.

















