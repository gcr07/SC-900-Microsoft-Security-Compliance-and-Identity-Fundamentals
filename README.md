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

## Como Funciona 

Como se ve en el vídeo, gracias a la autenticación moderna, el cliente se comunica con el proveedor de identidades mediante la asignación de una identidad que se puede autenticar. Cuando se ha comprobado la identidad (que puede ser un usuario o una aplicación), el proveedor de identidades emite un token de seguridad que el cliente envía al servidor.

El servidor valida el token de seguridad a través de su relación de confianza con el proveedor de identidades. Mediante el uso del token de seguridad y la información que contiene, el usuario o la aplicación accede a los recursos necesarios en el servidor. En este escenario, el proveedor de identidades almacena y administra el token y la información que contiene. El proveedor de identidades centralizado proporciona el servicio de autenticación.

Microsoft Azure Active Directory es un ejemplo de un proveedor de identidades basado en la nube. Otros ejemplos son Twitter, Google, Amazon, LinkedIn y GitHub.

## Inicio de sesión único Single sign on

Otra funcionalidad fundamental de un proveedor de identidades y "autenticación moderna" es la compatibilidad con el inicio de sesión único (SSO). Con el SSO, el usuario inicia sesión una vez y esa credencial se usa para tener acceso a varias aplicaciones o recursos. A la acción de configurar el SSO para que funcione entre varios proveedores de identidades se le conoce como federación.

# Descripción del concepto de servicios de directorio y Active Directory

Azure Active Directory es la siguiente evolución de las soluciones de administración de identidad y acceso. Proporciona a las organizaciones una solución de identidad como servicio (IDaaS) para todas sus aplicaciones en la nube y en el entorno local. En este curso, nos centraremos en Azure AD, el proveedor de identidades basado en la nube de Microsoft.

## Descripción del concepto de federación

![5-federated-identification](https://user-images.githubusercontent.com/63270579/194125924-b18dc4c5-451f-47f3-9385-a7aaf26354be.png)


La federación permite el acceso a los servicios a través de los límites de la organización o del dominio mediante el establecimiento de relaciones de confianza entre el proveedor de identidades del dominio correspondiente. Con la federación, no es necesario que un usuario mantenga un nombre de usuario y una contraseña diferentes al acceder a los recursos de otros dominios.

## Como Funciona 

La manera simplificada de considerar este escenario de federación es la siguiente:

El sitio web, en el dominio A, usa los servicios de autenticación del proveedor de identidades A (IdP-A).
El usuario, en el dominio B, se autentica con el proveedor de identidades B (IdP-B).
IdP-A tiene una relación de confianza configurada con IdP-B.
Cuando el usuario, que desea acceder al sitio web, proporciona sus credenciales, el sitio web confía en el usuario y permite el acceso. Este acceso se permite debido a la confianza que ya se ha establecido entre los dos proveedores de identidades.
Con la federación, la confianza no siempre es bidireccional. Aunque IdP-A puede confiar en IdP-B y permitir que el usuario del dominio B tenga acceso al sitio web del dominio A, lo contrario no es cierto, a menos que se configure la relación de confianza.

Un ejemplo común de federación en la práctica es cuando un usuario inicia sesión en un sitio de terceros con su cuenta de redes sociales, como Twitter. En este escenario, Twitter es un proveedor de identidades y el sitio de terceros podría estar usando otro proveedor de identidades, como Azure AD. Hay una relación de confianza entre Azure AD y Twitter.


# Descripción de Azure Active Directory

![azure-active-directory-diagram-expanded](https://user-images.githubusercontent.com/63270579/194129520-de50bb31-265e-480e-92ab-44f25cd625d0.png)


Microsoft Azure Active Directory (Azure AD), parte de Microsoft Entra, es el servicio de administración de identidades y acceso basado en la nube de Microsoft. Las organizaciones usan Azure AD para permitir que sus empleados, invitados y otros usuarios inicien sesión y tengan acceso a los recursos

Azure AD simplifica la forma en que las organizaciones administran la autorización y el acceso, ya que proporciona un sistema de identidad único para sus aplicaciones locales y en la nube. Igualmente, Azure AD se puede sincronizar con la instancia de Active Directory local existente, con otros servicios de directorio o se puede usar como un servicio independiente.

## Descripción de las ediciones de Azure AD disponibles

Azure AD está disponible en cuatro ediciones: gratuita, aplicaciones de Office 365, Premium P1 y Premium P2.

## Azure Active Directory Free
. La versión gratuita le permite administrar usuarios y crear grupos, sincronizarse con la instancia local de Active Directory, crear informes básicos, configurar el cambio de contraseña de autoservicio para usuarios en la nube y habilitar el inicio de sesión único en Azure, Microsoft 365 y muchas otras aplicaciones populares de SaaS. La edición gratuita se incluye con las suscripciones a Office 365, Azure, Dynamics 365, Intune y Power Platform.

## Aplicaciones de Office 365.

La edición de Aplicaciones de Office 365 le permite hacer todo lo que se incluye en la versión gratuita, más la opción de restablecer la contraseña de autoservicio para usuarios en la nube y la reescritura de dispositivos, que ofrece una sincronización bidireccional entre directorios locales y Azure AD. La edición de Aplicaciones de Office 365 de Azure Active Directory se incluye en las suscripciones a Office 365 E1, E3, E5, F1 y F3.

## Azure Active Directory Premium P1
. La edición Premium P1 incluye todas las características de las ediciones Gratis y Aplicaciones de Office 365. También admite la administración avanzada, como grupos dinámicos, administración de grupos de autoservicio, Microsoft Identity Manager (un conjunto de administración local de identidades y acceso) y funcionalidades de reescritura en la nube, que permiten el restablecimiento de contraseña de autoservicio a los usuarios locales.

## Azure Active Directory Premium P2.

La versión P2 le ofrece todas las características de la edición Premium P1 y Azure Active Directory Identity Protection para facilitar el acceso condicional basado en riesgos a las aplicaciones y a los datos críticos de la empresa. Asimismo, la edición P2 también le proporciona la instancia de Privileged Identity Management que le permitirá detectar, restringir y supervisar a los administradores y su acceso a los recursos y proporcionar acceso de tipo "Just-in-Time" cuando sea necesario.

Para obtener más información sobre cada una de las ediciones, visite la página de precios de Azure Active Directory.

También hay una opción para las licencias de característicasde "Pago por uso". Puede obtener otras licencias de características por separado, como la opción Negocio a cliente (B2C) de Azure Active Directory. B2C puede ayudarle a proporcionar soluciones de administración de acceso y de identidad para las aplicaciones orientadas al cliente. Para más información, consulte Documentación de Azure Active Directory B2C.

# Descripción de los tipos de identidad de Azure AD

Azure AD administra distintos tipos de identidades: usuarios, entidades de servicio, identidades administradas y dispositivos. En esta unidad, se detallará cada tipo de identidad de Azure AD.

## Usuario

Una identidad de usuario es una representación de algo que se administra mediante Azure AD. Los empleados e invitados se representan como usuarios en Azure AD. Si tiene varios usuarios con las mismas necesidades de acceso, puede crear un grupo. Los grupos se usan para conceder permisos de acceso a todos los miembros del grupo, en lugar de tener que asignar derechos de acceso individualmente.

La colaboración de negocio a negocio (B2B) de Azure AD es una característica de External Identities e incluye una funcionalidad para agregar usuarios invitados. Gracias a la colaboración B2B, una organización puede compartir aplicaciones y servicios de forma segura con usuarios invitados de otra organización.

## Entidad de servicio O cuenta de servicio

Una entidad de servicio es, básicamente, una identidad para una aplicación. Para que una aplicación delegue su identidad y funciones de acceso a Azure AD, primero se debe registrar con Azure AD a fin de habilitar su integración. Una vez que se registra, se crea una entidad de servicio en cada inquilino de Azure AD donde se usa la aplicación. La entidad de servicio habilita características básicas como la autenticación y autorización de la aplicación en los recursos protegidos por el inquilino de Azure AD.

Para que las entidades de servicio puedan acceder a los recursos protegidos por el inquilino de Azure AD, los desarrolladores de aplicaciones deben administrar y proteger las credenciales.

## Identidad administrada

![when-use-managed-identities-inline](https://user-images.githubusercontent.com/63270579/194132636-aacec470-dd1d-4cd1-855c-dffcc5f9cd6c.png)


Las identidades administradas son un tipo de entidad de servicio que se administran de forma automática en Azure AD y eliminan la necesidad de que los desarrolladores administren las credenciales. Las identidades administradas proporcionan una identidad para que la usen las aplicaciones al conectarse a recursos de Azure compatibles con la autenticación de Azure AD, sin costo adicional.

Para obtener una lista de los servicios de Azure que admiten identidades administradas, consulte la sección Más información de la unidad Resumen y recursos.

Hay dos tipos de identidades administradas: asignadas por el sistema y asignadas por el usuario.

### Asignadas por el sistema.

Algunos servicios de Azure permiten habilitar una identidad administrada directamente en una instancia de servicio. Cuando se habilita una identidad administrada asignada por el sistema, se crea una identidad en Azure AD que está vinculada al ciclo de vida de esa instancia de servicio. Por tanto, cuando se elimina el recurso, Azure elimina automáticamente la identidad. Por diseño, solo ese recurso de Azure puede usar esta identidad para solicitar tokens de Azure AD.

### Asignadas por el usuario.

También es posible crear una identidad administrada como un recurso independiente de Azure. Una vez que se crea una identidad administrada asignada por el usuario, puede asignarla a una o varias instancias de un servicio de Azure. En el caso de las identidades administradas asignadas por el usuario, la identidad se administra independientemente de los recursos que la utilicen.

## Dispositivo

Un dispositivo es un producto de hardware, como los dispositivos móviles, los equipos portátiles, los servidores o las impresoras. Una identidad de dispositivo proporciona a los administradores información que pueden usar al tomar decisiones de acceso o configuración. Hay varias formas de configurar las identidades de dispositivo en Azure AD.

### Dispositivos registrados en Azure AD.

El objetivo de los dispositivos registrados en Azure AD es proporcionar a los usuarios la compatibilidad con escenarios Bring Your Own Device (BYOD) o de dispositivos móviles. En estos escenarios, el usuario puede acceder a los recursos de la organización con un dispositivo personal. Los dispositivos registrados en Azure AD se registran sin necesidad de que una cuenta de la organización inicie sesión en el dispositivo. Los sistemas operativos compatibles con los dispositivos registrados de Azure AD incluyen Windows 10 y versiones posteriores, iOS, Android y macOS.
## Unido a Azure AD

Un dispositivo unido a Azure AD es el que se une mediante una cuenta de la organización, que luego se usa para iniciar sesión en el dispositivo. Los dispositivos unidos a Azure AD suelen ser propiedad de la organización. Los sistemas operativos compatibles con dispositivos unidos a Azure AD incluyen Windows 10 o versiones posteriores (excepto Home Edition) y máquinas virtuales con Windows Server 2019 que se ejecutan en Azure.
### Dispositivos unidos a Azure AD híbrido.

Las organizaciones con implementaciones locales de Active Directory existentes se pueden beneficiar de algunas de las funcionalidades proporcionadas por Azure AD mediante la implementación de dispositivos unidos a Azure AD híbrido. Estos dispositivos están unidos a la instancia local de Active Directory y Azure AD exige que la cuenta de la organización inicie sesión en el dispositivo.
El registro y la unión de dispositivos a Azure AD proporciona a los usuarios el inicio de sesión único (SSO) a los recursos en la nube. Además, los dispositivos que están unidos a Azure AD se benefician de la experiencia de inicio de sesión único en los recursos y aplicaciones que dependen de la instancia de Active Directory local.

Los administradores de TI pueden usar herramientas como Microsoft Intune, un servicio basado en la nube que se centra en la administración de dispositivos móviles (MDM) y la administración de aplicaciones móviles (MAM), para controlar cómo se usan los dispositivos de una organización.

# Descripción de los tipos de identidades externas

Azure AD External Identities es un conjunto de capacidades que permiten a las organizaciones permitir el acceso a usuarios externos, como clientes o asociados. Los clientes, asociados y otros usuarios invitados pueden "traer sus propias identidades" para iniciar sesión.

Esta capacidad para los usuarios externos se habilita a través de la compatibilidad de Azure AD con proveedores de identidades externos como otros inquilinos de Azure AD, Facebook, Google o proveedores de identidades de empresa. Los administradores pueden configurar la federación con proveedores de identidades para que los usuarios externos puedan iniciar sesión con sus cuentas empresariales o sociales existentes, en lugar de crear una nueva cuenta solo para la aplicación.

Existen dos identidades externas de Azure AD External Identities: B2B y B2C.

La colaboración B2B le permite compartir sus aplicaciones y recursos con usuarios externos.
En cambio, B2C es una solución de administración de identidades para aplicaciones de consumidor que están orientadas al cliente.

## Colaboración B2B
La colaboración B2B le permite compartir las aplicaciones y los servicios de la organización con usuarios invitados de otras organizaciones, a la vez que mantiene el control sobre sus propios datos. La colaboración B2B usa un proceso de invitación y canje. También puede habilitar los flujos de usuario de registro de autoservicio para permitir que los usuarios externos se suscriban a aplicaciones o recursos por sí mismos. Una vez que el usuario externo ha canjeado su invitación o ha completado el registro, se representa en el mismo directorio que los empleados, pero con un tipo de usuario de invitado. Como invitado, ahora puede acceder a los recursos con sus credenciales.

Los usuarios invitados pueden administrarse de la misma manera que los empleados, se pueden agregar a los mismos grupos, etc. Con B2B, se admite el inicio de sesión único en todas las aplicaciones conectadas a Azure AD.

## Administración de acceso de B2C

![customized-screen](https://user-images.githubusercontent.com/63270579/194134631-9cbc60b1-58ab-4f32-99b0-6463b6e03d01.png)

Azure AD B2C es una solución de administración de acceso de identidades de cliente (CIAM). Azure AD B2C permite a los usuarios externos iniciar sesión con sus identidades de cuenta de redes sociales, de empresa o locales preferidas, para obtener un inicio de sesión único en las aplicaciones. Azure AD B2C admite millones de usuarios y miles de millones de autenticaciones al día. Asimismo, se encarga del escalado y la seguridad de la plataforma de autenticación, de la supervisión y del control automático de amenazas, como la denegación del servicio, la difusión de contraseñas o los ataques por fuerza bruta.

Gracias a Azure AD B2C, los usuarios externos se administran en el directorio de Azure AD B2C, de forma independiente del directorio de asociados y empleados de la organización. Igualmente, se admite el inicio de sesión único para aplicaciones que sean propiedad de los clientes dentro del inquilino de Azure AD B2C.

***Azure AD External Identities es una característica de las ediciones de Azure AD Premium P1 y P2, y los precios se basan en función de los usuarios activos mensuales.***

# Descripción del concepto de identidad híbrida

Muchas organizaciones son una combinación de aplicaciones locales y en la nube. Independientemente de si una aplicación está hospedada en el entorno local o en la nube, los usuarios esperan y exigen un acceso sencillo. Las soluciones de identidad de Microsoft abarcan funcionalidades locales y basadas en la nube. Estas soluciones crean una identidad de usuario común para la autenticación y autorización en todos los recursos, independientemente de la ubicación. A esto lo llamamos identidad híbrida.

![azure-active-directory-connect-expanded](https://user-images.githubusercontent.com/63270579/194135162-9e991d80-a281-4a31-9b11-8903bad68678.png)


 En lo que respecta a la autenticación de identidades híbridas, Microsoft ofrece varias maneras de autenticarse.

Sincronización de hash de contraseña de Azure AD.
Autenticación transferida de Azure AD
Autenticación federada
Estas opciones de autenticación híbrida, descritas a continuación, necesitan una instancia local de Active Directory. Además, se necesita Azure AD Connect, una aplicación de Microsoft local que se ejecuta en un servidor y actúa como puente entre Azure AD y la instancia local de Active Directory.

### Sincronización de hash de contraseña de Azure AD

La sincronización de hash de contraseña de Azure AD es la manera más sencilla de habilitar la autenticación para los objetos de directorio local en Azure AD. Los usuarios pueden iniciar sesión en los servicios de Azure AD con el mismo nombre de usuario y la misma contraseña que usan para hacerlo en su instancia local de Active Directory. Azure AD controla el proceso de inicio de sesión de los usuarios.

El servicio de dominio de Active Directory (AD DS) almacena contraseñas en forma de representación de valor de hash de la contraseña de usuario real. Con la sincronización de hash de contraseñas de Azure AD, el hash de contraseña se extrae de la instancia local de Active Directory mediante Azure AD Connect. Se aplica seguridad adicional al hash de contraseña y, después, se sincroniza con el servicio de autenticación de Azure Active Directory. Cuando un usuario intenta iniciar sesión en Azure AD y escribe su contraseña, la contraseña se ejecuta con el mismo algoritmo de hash y seguridad adicional que se ha aplicado a la versión almacenada en Azure AD, como parte de la sincronización. Si el resultado coincide con el valor de hash almacenado en Azure AD, el usuario ha escrito la contraseña correcta y se autentica.

Con la sincronización de hash de contraseña, Azure AD Connect garantiza que el hash de contraseña se sincronice entre la instancia local de Active Directory y Azure AD. Esto permite que la autenticación del usuario se realice en Azure AD, y no en la propia instancia de Active Directory de la organización. Una ventaja de este enfoque es que la sincronización de hash de contraseña proporciona autenticación en la nube de alta disponibilidad. Los usuarios locales pueden autenticarse con Azure AD para acceder a aplicaciones basadas en la nube, incluso si la instancia local de Active Directory deja de funcionar.

### Autenticación de paso a través de Azure AD.

La autenticación transferida de Azure AD permite a los usuarios iniciar sesión en aplicaciones locales y basadas en la nube con las mismas contraseñas, como la sincronización de hash de contraseña. Pero una diferencia clave es que cuando los usuarios inician sesión con la autenticación transferida de Azure AD, las contraseñas se validan directamente en la instancia local de Active Directory. La validación de las contraseñas no se produce en la nube. Esto puede ser un factor importante para las organizaciones que quieran aplicar sus directivas de seguridad y contraseñas de Active Directory locales.


Es mucho rollo si quieres ver algo de esto en concreto ve a la docunentacion de Microsoft.

### Autenticación federada.

La federación se recomienda como autenticación para las organizaciones que tienen características avanzadas que no se admiten actualmente en Azure AD, incluido el inicio de sesión con tarjetas inteligentes o certificados, con un servidor local de autenticación multifactor (MFA) o mediante una solución de autenticación de terceros.

En la autenticación federada, Azure AD delega el proceso de autenticación a un sistema independiente de autenticación de confianza como, por ejemplo, una instancia local de Servicios de federación de Active Directory (AD FS), para validar la contraseña del usuario. Este método de inicio de sesión garantiza que toda la autenticación de usuarios tiene lugar de forma local.

La autenticación federada usa Azure AD Connect, pero también necesita servidores adicionales para admitir la federación, lo que da lugar a una superficie de infraestructura mayor.

Las organizaciones que deciden usar la federación con Servicios de federación de Active Directory (AD FS) tienen la posibilidad de configurar la sincronización de hash de contraseña como copia de seguridad en caso de error en la infraestructura de AD FS.

# Describir los métodos de autenticación de Azure AD

El uso de contraseñas debe complementarse o reemplazarse por métodos de autenticación más seguros disponibles en Azure AD.

## Teléfono

Azure AD admite dos opciones para la autenticación basada en teléfono.

### Autenticación basada en SMS.

El servicio de mensajes cortos (SMS) usado en la mensajería de texto del dispositivo móvil se puede usar como forma principal de autenticación. Con el inicio de sesión basado en SMS, los usuarios ***no necesitan conocer un nombre de usuario y una contraseña para acceder a las aplicaciones y servicios.*** En su lugar, el usuario escribe su número de teléfono móvil registrado, recibe un mensaje de texto con un código de verificación, y escribe el código en la interfaz de inicio de sesión.

### Comprobación por llamada de voz

Los usuarios pueden usar llamadas de voz como forma secundaria de autenticación, para comprobar su identidad, durante el autoservicio de restablecimiento de contraseña (SSPR) o Azure AD Multi-Factor Authentication. Con la verificación por llamada telefónica, se hace una llamada de voz automatizada al número de teléfono registrado por el usuario. Para completar el proceso de inicio de sesión, se le pide al usuario que presione # en el teclado. Las llamadas de voz no se admiten como una forma principal de autenticación en Azure AD.


### OATH

OATH (Open Authentication) es un estándar abierto que especifica cómo se generan los códigos de contraseña de un solo uso y duración definida (TOTP). Los códigos de contraseña de un solo uso se pueden usar para autenticar a un usuario. Los TOTP de OATH se implementan mediante software o hardware para generar los códigos.

#### Los tokens de software OATH

suelen ser aplicaciones. Azure AD genera la clave secreta, o valor de inicialización, que se introduce en la aplicación y se usa para generar cada OTP.

#### Los tokens de hardware OATH TOTP (compatibles con la versión preliminar pública) 

son dispositivos de hardware pequeños que parecen un fob de clave que muestra un código que se actualiza cada 30 o 60 segundos. Los tokens de hardware TOTP de OATH suelen incluir una clave secreta, o valor de inicialización, programada previamente en el token. Estas claves y otra información específica de cada token deben introducirse en Azure AD y, a continuación, activarse para su uso por parte de los usuarios finales.

Los tokens de hardware y software OATH solo se admiten como formas secundarias de autenticación en Azure AD para comprobar una identidad durante el autoservicio de restablecimiento de contraseña (SSPR) o Azure AD Multi-Factor Authentication.

## Autenticación sin contraseñas

En muchas organizaciones, el objetivo final es eliminar el uso de contraseñas como parte de los eventos de inicio de sesión. Cuando un usuario inicia sesión con un método sin contraseña, las credenciales se proporcionan mediante el uso de métodos como la información biométrica en Windows Hello para empresas o una clave de seguridad FIDO2. Un atacante no puede duplicar fácilmente estos métodos de autenticación.

Azure AD ofrece formas de autenticación nativa sin contraseña con el fin de simplificar la experiencia de inicio de sesión de los usuarios y reducir el riesgo de ataques.

### Windows Hello para empresas ( mas como de datos biometricos para iniciar en windows)


Windows Hello para empresas reemplaza las contraseñas con una autenticación de dos factores sólida en dispositivos. Esta autenticación en dos fases es una combinación de una clave o un certificado vinculado a un dispositivo y algo que la persona conoce (un PIN) o algo que la persona es (biometría). La entrada de PIN y el gesto biométrico desencadenan el uso de la clave privada para firmar criptográficamente los datos que se envían al proveedor de identidades. El proveedor de identidades comprueba la identidad del usuario y autentica al usuario.

Windows Hello para empresas ayuda a protegerse contra el robo de credenciales, ya que un atacante debe tener tanto el dispositivo como la información biométrica o el PIN, lo que dificulta el acceso sin el conocimiento del empleado.

Como método de autenticación sin contraseña, Windows Hello para empresas actúa como forma principal de autenticación. Además, Windows Hello para empresas se puede usar como forma secundaria de autenticación para comprobar una identidad durante la autenticación multifactor

## FIDO2 ( son como usb donde pones tu huella o pueden ser badges como el de la entrada a una empresa pero para iniciar sesion) 

Fast Identity Online (FIDO) es un estándar abierto para la autenticación sin contraseña. FIDO permite a los usuarios y a las organizaciones aprovechar el estándar para iniciar sesión en sus recursos mediante una clave de seguridad externa o una clave de plataforma integrada en un dispositivo, lo que elimina la necesidad de usar usuario y contraseña.

FIDO2 es el estándar más reciente que incorpora el estándar de autenticación web (WebAuthn) y es compatible con Azure AD. Las claves de seguridad FIDO2 son un método de autenticación sin contraseña basado en estándares que no permite la suplantación de identidad y que puede venir en cualquier factor de forma. Estas claves de seguridad FIDO2 suelen ser dispositivos USB, pero también pueden ser dispositivos basados en Bluetooth o comunicación de campo cercano (NFC), que se usan para la transferencia de datos inalámbricas de corto alcance. Con un dispositivo de hardware que controla la autenticación, se aumenta la seguridad de una cuenta, ya que no hay ninguna contraseña que pueda quedar expuesta ni adivinarse.

Con las claves de seguridad FIDO2, los usuarios pueden iniciar sesión en dispositivos Windows 10 unidos a Azure AD o Azure AD híbrido y lograr el inicio de sesión único en sus recursos de nube y locales. Los usuarios también pueden iniciar sesión en exploradores compatibles. Las claves de seguridad FIDO2 son una excelente opción para las empresas que son muy conscientes de la seguridad o tienen escenarios o empleados que no quieren o no pueden usar su teléfono como un segundo factor.

Como método de autenticación sin contraseña, FIDO2 actúa como forma principal de autenticación. Además, FIDO2 se puede usar como forma secundaria de autenticación para comprobar una identidad durante la autenticación multifactor.


#### En qué consiste FIDO2

Lo habitual es tener un nombre de usuario y poner una clave. Por ejemplo para entrar en redes sociales como Facebook, acceder al correo o iniciar un dispositivo. Lo que permite el estándar FIDO2 es poder dejar a un lado este método tradicional, pero sin poner en riesgo la seguridad. Se basa en la autenticación en dos factores y utiliza claves de seguridad.

El nombre de FIDO viene de Fast Identity Online y está formada por una alianza de algunas de las plataformas más conocidas a nivel mundial: Google, Amazon, Facebook o Mozilla, entre otros. Además, forman parte también el estándar WebAuthn y el protocolo CTAP. Se basa en el estándar anterior U2F y UAF, ambos realizados por FIDO.

Ahora bien, ¿cómo funciona exactamente? Su objetivo es permitir que nos autentiquemos en Internet, por ejemplo al usar una aplicación o entrar en un sitio web, sin tener que poner contraseña. Para ello podemos usar una pequeña llave de seguridad que se conecta por USB y conexión NFC. Pero también puedes utilizar el teléfono móvil para autenticarte.


## Aplicación Microsoft Authenticator

Como método de autenticación sin contraseña, la aplicación Microsoft Authenticator se puede usar como forma principal de autenticación para iniciar sesión en cualquier cuenta de Azure AD o como opción de verificación adicional durante el autoservicio de restablecimiento de contraseña (SSPR) o Azure AD eventos de Multi-Factor Authentication.

Para usar Microsoft Authenticator, un usuario debe descargar la aplicación de teléfono desde Microsoft Store y registrar su cuenta. Microsoft Authenticator está disponible para Android e iOS.

Con la información de inicio de sesión, la aplicación Authenticator convierte cualquier teléfono Android o iOS en una credencial segura sin contraseña. Para iniciar sesión en su cuenta de Azure AD, un usuario escribe su nombre de usuario, coincide con un número mostrado en la pantalla en el que se encuentra en su teléfono y, a continuación, usa su biométrica o PIN para confirmar.

LO QUE HACES PARA MODELO Y PARA ENTRAR A OUTLOOK

![image](https://user-images.githubusercontent.com/63270579/194353106-cc0641d9-863d-4bdc-ae30-1dd87611d733.png)


Cuando un usuario elige Authenticator como método de autenticación secundario, para verificar su identidad, se envía una notificación push al teléfono o tableta. Si la notificación es legítima, el usuario selecciona Aprobar; de lo contrario, selecciona Denegar.

![image](https://user-images.githubusercontent.com/63270579/194353136-3e14a639-92ba-41a3-9792-aa7e8e7b5700.png)











