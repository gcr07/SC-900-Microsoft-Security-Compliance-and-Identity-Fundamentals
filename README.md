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

## Describir la autenticación multifactor (MFA) en Azure AD

La autenticación multifactor requiere más de una forma de comprobación para demostrar que una identidad es legítima, como un dispositivo de confianza o una detección de huellas digitales. Esto implica que, aunque la contraseña de una identidad se haya puesto en peligro, un hacker no podrá acceder al recurso.

El funcionamiento de la autenticación multifactor de Azure Active Directory solicita lo siguiente:

Algo que sabe: normalmente una contraseña o un PIN y
Algo que tiene: como un dispositivo de confianza que no se duplica fácilmente; por ejemplo, un teléfono o una clave de hardware, o
Algo que forma parte de usted: información biométrica como una huella digital o una detección de rostro.

##  Autoservicio de restablecimiento de contraseña (SSPR) en Azure AD


El autoservicio de restablecimiento de contraseña (SSPR) es una característica de Azure AD que permite a los usuarios cambiar o restablecer su contraseña, sin necesidad de que intervenga el administrador o el departamento de soporte técnico.

##  Funcionalidades de administración y protección de contraseñas de Azure AD

La protección de contraseñas es una característica de Azure AD que reduce el riesgo de que los usuarios establezcan contraseñas no seguras. La característica Protección de contraseñas de Azure AD detecta y bloquea las contraseñas no seguras conocidas y sus variantes;además, puede bloquear otros términos poco seguros específicamente para la organización.

Para satisfacer sus necesidades empresariales y de seguridad, puede definir entradas en una lista personalizada de contraseñas prohibidas. Cuando los usuarios cambian o restablecen sus contraseñas, se consultan estas listas para exigir el uso de contraseñas seguras.

La lista global de contraseñas prohibidas se aplica automáticamente y no se puede deshabilitar.

Los administradores también pueden crear listas personalizadas de contraseñas prohibidas para satisfacer necesidades específicas de seguridad empresarial.
pueden integrar la Protección de contraseñas de Azure AD en un entorno de Active Directory local. 


# Funcionalidades de administración de acceso de Azure AD

## Acceso condicional en Azure AD

El acceso condicional es una característica de Azure AD que proporciona una capa de seguridad adicional antes de permitir que los usuarios autenticados tengan acceso a los datos o a otros recursos. El acceso condicional se implementa a través de las directivas que se crean y administran en Azure AD. Una directiva de acceso condicional analiza las señales que incluyen el usuario, la ubicación, el dispositivo, la aplicación y el riesgo para automatizar las decisiones de autorización de acceso a los recursos (aplicaciones y datos).



# Ventajas de los roles de Azure AD y el control de acceso basado en rolesentajas de los roles de Azure AD y el control de acceso basado en roles

Los roles de Azure AD controlan los permisos para administrar los recursos de Azure AD. Por ejemplo, permitir la creación de cuentas de usuario o ver la información de facturación. Azure AD admite roles integrados y personalizados.

La administración del acceso mediante roles se conoce como control de acceso basado en roles (RBAC). Los roles integrados y personalizados de Azure AD son una forma de RBAC en que los roles de Azure AD controlan el acceso a los recursos de Azure AD. Esto se denomina RBAC de Azure AD.

## Roles integrados

En Azure AD hay muchos roles integrados, que son los que tienen un conjunto fijo de permisos de rol. Algunos de los roles integrados más comunes son los siguientes:

Administrador global: los usuarios con este rol tienen acceso a todas las características administrativas de Azure Active Directory. El usuario que se suscribe al inquilino de Azure Active Directory se convierte en administrador global de manera automática.
Administrador de usuarios: los usuarios con este rol pueden crear y administrar todos los aspectos de los usuarios y grupos. Además, este rol incluye la capacidad de administrar incidencias de soporte técnico y supervisar el estado del servicio.
Administrador de facturación: los usuarios que tienen este rol realizan compras, administra suscripciones e incidencias de soporte técnico y supervisan el estado del servicio.
Todos los roles integrados son agrupaciones preconfiguradas de permisos que se diseñaron para tareas específicas. El conjunto fijo de permisos incluidos en los roles integrados no se puede modificar.

## Roles personalizados

Si bien hay muchos roles de administrador integrados en Azure AD, los roles personalizados proporcionan flexibilidad a la hora de conceder acceso. Una definición de roles personalizada es una colección de permisos que se seleccionan en una lista preestablecida. La lista de permisos entre los que se puede elegir son los mismos que usan los roles integrados. La diferencia es que puede elegir qué permisos quiere incluir en un rol personalizado.

***Los servicios de Microsoft 365 disponibles incluyen Azure AD, Exchange, SharePoint, Microsoft Defender, Teams, Intune y muchos más.***


![image](https://user-images.githubusercontent.com/63270579/194366953-1ac08ea9-7e15-456b-88c4-d3bf8a9a89dd.png)


## Diferencias entre los roles de RBAC de Azure y Azure AD

RBAC de Azure AD: los roles de Azure AD controlan el acceso a recursos de Azure AD como usuarios, grupos y aplicaciones.
RBAC de Azure: los roles de Azure controlan el acceso a recursos de Azure como máquinas virtuales o almacenamiento mediante la administración de recursos de Azure.



# Gobernanza de identidades

La gobernanza de identidades consiste en equilibrar la seguridad de identidad con la productividad de los usuarios de una manera que se pueda justificar y auditar. Azure AD ofrece muchas funcionalidades de protección y gobernanza de identidades, incluido Privileged Identity Management (PIM), Identity Protection y los términos de uso.

## Azure AD Identity Governance

ofrece a las organizaciones la posibilidad de realizar las siguientes tareas:

Administrar el ciclo de vida de las identidades.

Administrar el ciclo de vida de los accesos.

Proteger el acceso con privilegios para la administración.


## Ciclo de vida de las identidades

![image](https://user-images.githubusercontent.com/63270579/194389052-4b3cdefb-1cd8-4f49-98b0-6d0c4fa8300c.png)

Azure AD Premium incluye también Microsoft Identity Manager, que permite importar registros desde los sistemas de recursos humanos locales, como SAP HCM, Oracle eBusiness y Oracle PeopleSoft. Para obtener más información, consulte la documentación de Microsoft Identity Manager que se muestra en la sección Más información de la unidad de resumen y recursos.

En general, la administración del ciclo de vida de una identidad consiste en actualizar el acceso que necesitan los usuarios, ya sea a través de la integración con un sistema de recursos humanos, o a través de aplicaciones de aprovisionamiento de usuarios.


## Revisiones de acceso de Azure AD

Las revisiones de acceso de Azure Active Directory (AD) permiten a las organizaciones administrar de forma eficiente la pertenencia a grupos, el acceso a las aplicaciones empresariales y la asignación de roles. Las revisiones de acceso periódicas garantizan que solo las personas adecuadas tienen acceso a los recursos. Los derechos de acceso excesivos suponen un riesgo de seguridad conocido. Sin embargo, cuando las personas se transfieren de un equipo a otro, o cuando asumen o ceden responsabilidades, los derechos de acceso pueden ser difíciles de controlar.

Las revisiones de acceso se pueden crear a través de las revisiones de acceso de Azure AD o de Azure AD Privileged Identity Management (PIM).

Cuando se crea una revisión de acceso, se puede configurar para que cada usuario revise su propio acceso, o para que uno o varios usuarios revisen el acceso de todos. Del mismo modo, se puede solicitar a todos los invitados que revisen su propio acceso, o que lo examinen uno o varios usuarios.

## Privileged Identity Management

Privileged Identity Management (PIM) es un servicio de Azure Active Directory (Azure AD) que permite administrar, controlar y supervisar el acceso a recursos importantes de la organización. Esto incluye a los recursos de Azure AD, Azure y los de otros servicios en línea de Microsoft, como Microsoft 365 o Microsoft Intune. PIM mitiga los riesgos de los permisos de acceso excesivos, innecesarios o mal utilizados. Requiere una justificación para saber por qué los usuarios quieren los permisos y aplica la autenticación multifactor para activar cualquier rol.


Privileged Identity Management es una característica de Azure AD Premium P2.

## Azure AD Identity Protection


Identity Protection es una herramienta que permite a las organizaciones realizar tres tareas clave:

Automatizar la detección y corrección de riesgos basados en la identidad.
Investigar los riesgos de usar los datos en el portal.
Exportar los datos de detección de riesgos a utilidades de terceros para su posterior análisis.

Las señales que generan estos servicios se cargan en Identity Protection. A continuación, las herramientas como el acceso condicional pueden usar estas señales para tomar decisiones sobre el acceso. Las señales también se cargan en las herramientas de administración de eventos e información de seguridad (SIEM), como Microsoft Sentinel, para investigación adicional.

Identity Protection clasifica el riesgo en tres niveles: bajo, medio y alto. También puede calcular el riesgo de inicios de sesión y el riesgo de identidades del usuario.

Un riesgo de inicio de sesión representa la probabilidad de que el propietario de la identidad no haya autorizado una solicitud de autenticación determinada. El riesgo de inicio de sesión se puede calcular en tiempo real o sin conexión, usando orígenes de inteligencia sobre amenazas internos y externos de Microsoft


Un riesgo de usuario representa la probabilidad de que una identidad o cuenta determinada esté en peligro. Los riesgos se calculan sin conexión, usando orígenes de inteligencia sobre amenazas internos y externos de Microsoft. Filtración de credenciales y Inteligencia sobre amenazas de Azure AD

Identity Protection proporciona a las organizaciones tres informes que pueden usar para investigar los riesgos de identidad en su entorno. Estos informes son sobre los usuarios de riesgo, los inicios de sesión de riesgo y las detecciones de riesgo. La investigación de eventos es clave para comprender e identificar los puntos débiles de la estrategia de seguridad.

***Identity Protection es una característica de Azure AD Premium P2.***

![image](https://user-images.githubusercontent.com/63270579/194397428-10178097-e563-40d9-859a-d7092a614c37.png)

![image](https://user-images.githubusercontent.com/63270579/194397509-5e941484-2951-4109-bf78-59ae24b66dd4.png)


# FUncionalidades de seguridad en Azure

## Protección contra DDoS de Azure

El objetivo de un ataque de denegación de servicio distribuido (DDoS) es sobrecargar los recursos en las aplicaciones y servidores, lo que les deja sin responder o ralentiza a los usuarios auténticos. Un ataque DDoS normalmente se dirige a cualquier dispositivo de acceso público al que se pueda acceder a través de Internet.

Los tres tipos más frecuentes de ataque DDoS son:

### Ataques volumétricos: 

Se tratan de ataques basados en volúmenes que inundan la red con tráfico aparentemente legítimo, sobrepasando el ancho de banda disponible. El tráfico legítimo no logra comunicarse. Estos tipos de ataques se miden en bits por segundo.

### Ataques de protocolo: 

Los ataques de protocolo representan un destino inaccesible al agotar los recursos del servidor con solicitudes de protocolo falsas que aprovechan los puntos débiles de los protocolos de nivel 3 (red) y nivel 4 (transporte). Estos tipos de ataques se miden normalmente en paquetes por segundo.

### Ataques de nivel de recurso (aplicación) :

Estos ataques van dirigidos a paquetes de aplicaciones web y su objetivo es interrumpir la transmisión de datos entre hosts.

##  Azure DDoS Protection

![image](https://user-images.githubusercontent.com/63270579/194715630-e95ca26a-3444-4105-be99-05d626851d7f.png)


El servicio Azure DDoS Protection está diseñado para ayudar a proteger sus aplicaciones y servidores mediante el análisis del tráfico de red y el descarte de todo lo que parezca un ataque DDoS.

Azure DDoS Protection usa la escala y la elasticidad de la red global de Microsoft para incorporar capacidad de mitigación de DDoS a cada región de Azure. Durante un ataque DDoS, Azure puede escalar las necesidades informáticas para satisfacer la demanda. Para administra el consumo de la nube, DDoS Protection se asegura de que la carga de red solo refleje el uso real de los clientes.


Azure DDoS Protection se incluye en dos niveles:

Básico: El nivel de servicio Básico está habilitado automáticamente para cada propiedad de Azure, sin costo adicional, como parte de la plataforma Azure.

Estándar: Este nivel de servicio Estándar ofrece funcionalidades adicionales de mitigación adaptadas específicamente a los recursos de Microsoft Azure Virtual Network. DDoS Protection Estándar es fácil de habilitar y no requiere ningún cambio en la aplicación.

El servicio Estándar de DDoS Protection tiene un cargo mensual fijo que incluye protección para 100 recursos. La protección de recursos adicionales se cobra mensualmente por cada recurso.

## Azure Firewall

![image](https://user-images.githubusercontent.com/63270579/194715849-ede03371-b63a-48b2-bc8c-944e094bf688.png)

Azure Firewall es un servicio de seguridad de red administrado y basado en la nube que protege los recursos de redes virtuales (VNet) de Azure frente a los atacantes. Puede implementar Azure Firewall en cualquier red virtual, pero el mejor enfoque es usarlo en una red virtual centralizada. Todas las demás redes virtuales y locales se enrutarán a través de ella. La ventaja de este modelo es la capacidad de ejercer de forma centralizada el control del tráfico de red para todas las redes virtuales en diferentes suscripciones.

![image](https://user-images.githubusercontent.com/63270579/194715971-94a6ae47-9c7e-4d8e-80d1-52e14976f8e3.png)

## Web Application Firewall WAF

El firewall de aplicaciones web (WAF) ofrece una protección centralizada de las aplicaciones web contra las vulnerabilidades de seguridad más habituales. Un WAF centralizado ayuda a simplificar la administración de la seguridad, mejora el tiempo de respuesta ante una amenaza de seguridad y permite aplicar revisiones a una vulnerabilidad conocida en un lugar, en lugar de proteger cada aplicación web individual. Un WAF también proporciona a los administradores de la aplicación a un mejor control de la protección contra amenazas e intrusiones.

## Segmentación de red en Azure

La segmentación de la red puede asegurar las interacciones entre los perímetros. Este enfoque puede reforzar la postura de seguridad de una organización, contener los riesgos en caso de infracción y evitar que los atacantes accedan a toda la carga de trabajo.

### Azure Virtual Network (VNet)

![image](https://user-images.githubusercontent.com/63270579/194716226-1fbb94ed-873b-4d44-b2ad-bd1bf7d2575a.png)


Azure Virtual Network (VNet) es la pieza clave para la red privada de su organización en Azure. VNet es similar a una red tradicional que funcionaría en su propio centro de datos, pero aporta las ventajas adicionales de la infraestructura de Azure, como la escala, la disponibilidad y el aislamiento.

Azure VNet permite a las organizaciones segmentar su red. Las organizaciones pueden crear varias VNets por región y por suscripción, y se pueden crear varias redes más pequeñas (subredes) dentro de cada VNet.


### Grupos de seguridad de red de Azure ( esto a nivel de maquinas virtuales) aunque tambien de subredes

Los grupos de seguridad de red (NSG) permiten filtrar el tráfico de red hacia y desde los recursos de Azure en una red virtual de Azure; por ejemplo, una máquina virtual. Un NSG consta de reglas que definen cómo se filtra el tráfico. Solo puede asociar un grupo de seguridad de red a cada subred e interfaz de red de la red virtual en una máquina virtual. Sin embargo, el mismo grupo de seguridad de red se puede asociar a tantas subredes e interfaces de red distintas como elija.

En el diagrama muy simplificado que se muestra a continuación, puede ver una red virtual de Azure con dos subredes que están conectadas a Internet, y cada subred tiene una máquina virtual. La subred 1 tiene un NSG asignado que filtra el acceso entrante y saliente a VM1, que necesita un mayor nivel de acceso. En cambio, VM2 podría representar una máquina de acceso público que no requiere un NSG.


Las VNets proporcionan una contención a nivel de red de los recursos sin que se permita el tráfico a través de las VNets o de entrada a la VNet, de forma predeterminada. La comunicación tiene que ser aprovisionada de forma explícita. Esto permite un mayor control sobre la forma en que los recursos de Azure en una VNet se comunican con otros recursos de Azure, Internet y las redes locales.


Un NSG se compone de reglas de seguridad de entrada y salida. Las reglas de seguridad del NSG se evalúan por prioridad con cinco elementos de información: origen, puerto de origen, destino, puerto de destino y protocolo, para permitir o denegar el tráfico. De manera predeterminada, Azure crea una serie de reglas, tres reglas de entrada y tres de salida, para proporcionar un nivel de línea de base de seguridad. No puede quitar las reglas predeterminadas, pero puede invalidarlas si crea otras con prioridades más altas.

## ¿Cuál es la diferencia entre los grupos de seguridad de red (NSG) y Azure Firewall?

Ahora que ha obtenido información sobre los grupos de seguridad de red y Azure Firewall, es posible que se pregunte en qué difieren, ya que ambos protegen los recursos de red virtual. El servicio Azure Firewall complementa la funcionalidad de grupo de seguridad de red. Juntos proporcionan una mejor seguridad de red de "defensa en profundidad". Los grupos de seguridad de red proporcionan filtrado de tráfico distribuido de nivel de red para limitar el tráfico a los recursos dentro de las redes virtuales de cada suscripción. Azure Firewall es un firewall de red como servicio con estado y centralizado, que proporciona protección de nivel de red y de aplicación entre las diferentes suscripciones y redes virtuales



## Azure Bastion 

![image](https://user-images.githubusercontent.com/63270579/194716770-84cdb4e3-3ff0-447c-adcc-b7465e2745ed.png)


### EL problema 

En un modelo tradicional, debe exponer los puertos del Protocolo de escritorio remoto (RDP) o Secure Shell (SSH) a Internet. Estos protocolos se pueden usar para obtener acceso remoto a las VM. Este proceso crea una amenaza de superficie significativa que los atacantes que buscan activamente máquinas accesibles con puertos de administración abiertos, como RDP o SSH, pueden explotar. Cuando se consigue poner en peligro a una máquina virtual, se usa como punto de entrada para atacar más recursos dentro de su entorno.

### La solucion 

Azure Bastion es un servicio que se implementa que le permite conectarse a una máquina virtual mediante el explorador y Azure Portal. Azure Bastion es un nuevo servicio PaaS totalmente administrado por la plataforma que se aprovisiona en las redes virtuales. Azure Bastion proporciona conectividad RDP y SSH segura e ininterrumpida a las máquinas virtuales, directamente desde Azure Portal mediante la Seguridad de la capa de transporte (TLS). Cuando se conecta a través de Azure Bastion, las máquinas virtuales no necesitan una dirección IP pública, un agente ni software cliente especial.


## Características clave de Azure Bastion

![image](https://user-images.githubusercontent.com/63270579/194716916-630670b1-0764-489d-bcfe-3c4b1e9c5ae7.png)

## Acceso Just-In-Time

El acceso Just-In-Time (JIT) permite bloquear el tráfico entrante a las máquinas virtuales; ya que reduce la exposición a ataques al mismo tiempo que se proporciona un acceso sencillo para conectarse a las máquinas virtuales cuando sea necesario.

Cuando se habilita el acceso a la máquina virtual Just-in-Time, se pueden seleccionar los puertos en la máquina virtual en los que se bloqueará el tráfico entrante. Microsoft Defender for Cloud, una herramienta para la administración de posiciones y protección frente a amenazas, garantiza que existen reglas para "denegar todo el tráfico entrante" de los puertos seleccionados en el grupo de seguridad de red (NSG) y las reglas de Azure Firewall. Estas reglas restringen el acceso a los puertos de administración de las máquinas virtuales de Azure y los defienden frente a ataques.

En caso de que ya existan otras reglas relativas a los puertos seleccionados, las reglas existentes tendrán prioridad sobre las nuevas reglas para "denegar todo el tráfico entrante". Si no hay ninguna regla existente en los puertos seleccionados, las nuevas reglas tendrán prioridad principal en los grupos de seguridad de red y Azure Firewall.

Cuando un usuario solicita acceso a una máquina virtual, Defender for Cloud comprueba que este tenga permisos de control de acceso basado en rol (RBAC de Azure) para ella. Si la solicitud se aprueba, Defender for Cloud configura los grupos de seguridad de red y Azure Firewall para permitir el tráfico entrante a los puertos seleccionados desde las direcciones (o rangos) IP relevantes durante el periodo especificado. Una vez transcurrido ese tiempo, Defender for Cloud restaura los NSG a su estado anterior. Las conexiones que ya están establecidas no se interrumpen.

***JIT necesita que Microsoft Defender para servidores esté habilitado en la suscripción.***

## Descripción de las maneras en que Azure cifra los datos Cifrado en Azure

### Azure Storage Service Encryption

ayuda a proteger los datos en reposo al cifrarlos automáticamente antes de almacenarlos en discos administrados de Azure, Azure Blob Storage, Azure Files o Azure Queue Storage, y descifrarlos antes de recuperarlos.

### Azure Disk Encryption 

le ayuda a cifrar discos de las máquinas virtuales de IaaS con Windows y Linux. Azure Disk Encryption usa la característica estándar del sector BitLocker de Windows y la característica dm-crypt de Linux para ofrecer cifrado de volumen para los discos de datos y del sistema operativo.

## El cifrado de datos transparente (TDE)

ayuda a proteger Azure SQL Database y Azure Data Warehouse frente a la amenaza de actividad malintencionada. También realiza cifrado y descifrado de la base de datos en tiempo real, copias de seguridad asociadas y archivos de registro de transacciones en reposo sin necesidad de efectuar cambios en la aplicación.

## Azure Key Vault

Azure Key Vault es un servicio centralizado en la nube para almacenar secretos de aplicación. Key Vault ayuda a controlar los secretos de la aplicación al mantenerlos en una sola ubicación centralizada y al proporcionar funcionalidades de acceso seguro, control de permisos y registro de acceso. Es útil para diferentes tipos de escenarios:

Azure Key Vault es un servicio centralizado en la nube para almacenar secretos de aplicación. Key Vault ayuda a controlar los secretos de la aplicación al mantenerlos en una sola ubicación centralizada y al proporcionar funcionalidades de acceso seguro, control de permisos y registro de acceso. Es útil para diferentes tipos de escenarios:

### Administración de secretos. 
Puede usar Key Vault para almacenar de forma segura y controlar de manera estricta el acceso a tokens, contraseñas, certificados, claves de interfaz de programación de aplicaciones (API) y otros secretos.

#### Administración de claves. 

Puede usar Key Vault como solución de administración de claves. Key Vault facilita la creación y el control de las claves de cifrado usadas para cifrar los datos.
### Administración de certificados. 

Key Vault permite aprovisionar, administrar e implementar certificados públicos y privados de Capa de sockets seguros y de Seguridad de la capa de transporte (SSL/TLS) para los recursos de Azure y los recursos conectados internamente, con más facilidad.
### Almacenamiento de secretos

respaldados por módulos de seguridad de hardware (HSM). Las claves y los secretos se pueden proteger mediante software, o bien con dispositivos HSM validados por FIPS 140-2 nivel 2.

Use las distintas formas en que Azure puede cifrar los datos para protegerlos con independencia de su ubicación o estado.


## Funcionalidades de administración de seguridad de Azure

### Descripción de la administración de la posición de seguridad en la nube Cloud Security Posture Management (CSPM)

La administración de la posición de seguridad en la nube (CSPM) es una clase relativamente nueva de herramientas diseñadas para mejorar la administración de la seguridad en la nube. Evalúa los sistemas y alerta automáticamente al personal de seguridad de su Departamento de TI cuando se detecta una vulnerabilidad. CSPM usa herramientas y servicios en el entorno de nube para supervisar y priorizar las mejoras y características de seguridad.

CSPM usa una combinación de herramientas y servicios:

#### Control de acceso basado en la confianza cero: 

Considera el nivel de amenaza activo durante las decisiones de control de acceso.

#### Puntuación del riesgo en tiempo real: 

Proporciona visibilidad sobre los principales riesgos.

#### Administración de amenazas y vulnerabilidades (TVM):

Establece una vista holística de la superficie y el riesgo de ataque de la organización, y la integra en las operaciones y la toma de decisiones de ingeniería.
#### Detección de riesgos: 

para comprender la exposición de los datos de la propiedad intelectual de la empresa en servicios en la nube autorizados y no autorizados

#### Directiva técnica:

Permite aplicar barreras para auditar y exigir los estándares y directivas de la organización a los sistemas técnicos.

#### Arquitecturas y sistemas de modelado de amenazas: 

Se usan junto con otras aplicaciones específicas.

Use CSPM para mejorar la administración de la seguridad en la nube mediante la evaluación del entorno y el envío automático de alertas al personal de seguridad en caso de presentarse vulnerabilidades.

## Descripción de Microsoft Defender for Cloud

Microsoft Defender for Cloud es una herramienta para la administración de la posición de seguridad y la protección contra amenazas. Esta refuerza la posición de seguridad de los recursos en la nube y, gracias a los planes integrados de Microsoft Defender, Defender for Cloud protege las cargas de trabajo híbridas que se ejecutan en Azure y otras plataformas en la nube.

## Microsoft Defender for Cloud

Rellena tres necesidades vitales a medida que administra la seguridad de los recursos y las cargas de trabajo en la nube y en el entorno local:

### Evaluación continua:

conozca su posición de seguridad, identifique y realice un seguimiento de las vulnerabilidades.

### Seguridad:

proteja todos los recursos y servicios conectados.

### Defender

detecte y resuelva las amenazas a recursos, cargas de trabajo y servicios.

![image](https://user-images.githubusercontent.com/63270579/194724347-4dd87a71-5f65-417e-a0df-a662bd04cbf2.png)

## Cloud Workload Protection (CWP)


El segundo pilar de la seguridad en la nube es la protección de cargas de trabajo en la nube. A través de las funcionalidades de protección de cargas de trabajo en la nube, Microsoft Defender for Cloud puede detectar y resolver amenazas a recursos, cargas de trabajo y servicios. Las protecciones de las cargas de trabajo en la nube se entregan mediante planes integrados de Microsoft Defender, específicos de los tipos de recursos de las suscripciones y proporcionan características de seguridad mejorada para las cargas de trabajo. 

## Descripción de la seguridad mejorada de Microsoft Defender for Cloud

Microsoft Defender for Cloud se ofrece en dos modos:

#### Microsoft Defender for Cloud (gratis):

Microsoft Defender for Cloud está habilitado de forma gratuita en todas las suscripciones de Azure. Mediante modo gratuito tendrá la puntuación segura y sus características relacionadas: la directiva de seguridad, la evaluación de seguridad continua y las recomendaciones de seguridad prácticas para que pueda proteger los recursos de Azure.

### Microsoft Defender for Cloud con características de seguridad mejorada:  

la habilitación de la seguridad mejorada amplía las funcionalidades del modo gratuito a las cargas de trabajo que se ejecutan en nubes de Azure, híbridas y otras plataformas de nube, lo que proporciona una administración de seguridad unificada y protección contra amenazas en todas las cargas de trabajo. Las protecciones de las cargas de trabajo en la nube se entregan mediante planes integrados de Microsoft Defender, específicos de los tipos de recursos de las suscripciones y proporcionan características de seguridad mejorada para las cargas de trabajo.

![image](https://user-images.githubusercontent.com/63270579/194724650-c0bd17f1-b056-47a4-800f-0de025fbea0c.png)


## Azure Security Benchmark y las líneas de base de seguridad para Azure

### Azure Security Benchmark

Alerta de spoiler, es una hoja de cálculo de Excel. Algunos de los elementos clave de información de ASB V3 son los siguientes:
Otros fragmentos de información de ASB incluyen vínculos a información sobre la implementación y sobre las partes interesadas de la seguridad e instrucciones sobre la asignación a Azure Policy. No se muestran en la imagen siguiente. La imagen siguiente es un extracto de Azure Security Benchmark (ASB v3) y se muestra como un ejemplo del tipo de contenido que se incluye en ASB v3. 

![image](https://user-images.githubusercontent.com/63270579/194726528-8b3df876-74e6-4cdc-931b-79f87ce7a659.png)

la línea de base de seguridad para Azure Active Directory aplica instrucciones de la versión 2.0 de Azure Security Benchmark a Azure Active Directory.

## Microsoft Sentinel ( SIEM )

Un sistema SIEM es una herramienta que una organización utiliza para recopilar datos de todo el patrimonio, incluida la infraestructura, el software y los recursos. Realiza análisis, busca correlaciones o anomalías y genera alertas e incidencias.

##  La respuesta automatizada de orquestación de seguridad (SOAR)?

Un sistema SOAR recibe alertas de muchos orígenes, como un sistema SIEM. El sistema SOAR desencadena entonces flujos de trabajo y procesos automatizados basados en acciones para ejecutar tareas de seguridad que mitiguen el problema.

A fin de proporcionar un enfoque completo para la seguridad, una organización debe usar una solución que adopte o combine las funcionalidades SIEM y SOAR.

![image](https://user-images.githubusercontent.com/63270579/194726828-1781f71f-c26f-4609-ac09-de8a88b523c3.png)

La administración efectiva del perímetro de seguridad de red de una organización requiere la combinación adecuada de herramientas y sistemas. Microsoft Sentinel es una solución SIEM/SOAR escalable y nativa de la nube que ofrece análisis de seguridad inteligentes e inteligencia sobre amenazas en toda la empresa. Proporciona una única solución para la detección de alertas, la visibilidad de las amenazas, la búsqueda proactiva y la respuesta a las amenazas.

En este diagrama se muestra la funcionalidad de un extremo a otro de Microsoft Sentinel.

Recopile datos a escala de nube de todos los usuarios, dispositivos, aplicaciones y de toda la infraestructura, tanto en el entorno local como en diversas nubes.
Detecte amenazas que antes no se abarcaban y reduzca los falsos positivos mediante un análisis y una inteligencia de amenazas sin precedentes.
Investigue amenazas con inteligencia artificial (IA) y busque actividades sospechosas a gran escala, aprovechando el trabajo de ciberseguridad que ha realizado Microsoft durante décadas.

Responda a los incidentes con rapidez con la orquestación y la automatización de tareas comunes de seguridad integradas.
Microsoft Sentinel ayuda a habilitar las operaciones de seguridad de un extremo a otro, en un centro de operaciones de seguridad (SOC) moderno. A continuación se enumeran algunas de las características clave de Microsoft Sentinel.

En este diagrama se muestra la funcionalidad de un extremo a otro de Microsoft Sentinel.

#### Recopile 

datos a escala de nube de todos los usuarios, dispositivos, aplicaciones y de toda la infraestructura, tanto en el entorno local como en diversas nubes.

#### Detecte

amenazas que antes no se abarcaban y reduzca los falsos positivos mediante un análisis y una inteligencia de amenazas sin precedentes.
#### Investigue 

amenazas con inteligencia artificial (IA) y busque actividades sospechosas a gran escala, aprovechando el trabajo de ciberseguridad que ha realizado Microsoft durante décadas.
### Responda

a los incidentes con rapidez con la orquestación y la automatización de tareas comunes de seguridad integradas.
Microsoft Sentinel ayuda a habilitar las operaciones de seguridad de un extremo a otro, en un centro de operaciones de seguridad (SOC) moderno. A continuación se enumeran algunas de las características clave de Microsoft Sentinel.

## Descripción de los costos de Sentinel

Microsoft Sentinel proporciona análisis de seguridad inteligente en toda la empresa. Los datos de este análisis se almacenan en un área de trabajo de Log Analytics de Azure Monitor. La facturación se basa en el volumen de datos ingeridos para su análisis en Microsoft Sentinel y almacenados en el área de trabajo de Log Analytics de Azure Monitor. Hay dos maneras de pagar por el servicio Microsoft Sentinel: reservas de capacidad y pago por uso.

### Reservas de capacidad:

con las reservas de capacidad, se le factura una tarifa fija en función del nivel seleccionado, lo que permite un costo total predecible para Microsoft Sentinel.

### Pago por uso: 

con los precios de pago por uso, se le factura por gigabyte (GB) el volumen de datos ingeridos para el análisis en Microsoft Sentinel y almacenados en el área de trabajo de Log Analytics de Azure Monitor.


# Describir los servicios de Microsoft 365 Defender

![image](https://user-images.githubusercontent.com/63270579/194733372-0e8522cc-1ad8-4153-883d-a24d257276d8.png)

Microsoft 365 Defender es un conjunto de Enterprise Defense que protege frente a sofisticados ciberataques. Con Microsoft 365 Defender, puede coordinar de forma nativa la detección, prevención, investigación y respuesta a las amenazas en puntos de conexión, identidades, correo electrónico y aplicaciones.

Microsoft 365 Defender permite a los administradores evaluar las señales de amenazas de puntos de conexión, identidades, correo electrónico y aplicaciones para determinar el ámbito y el impacto de un ataque. Proporciona información más detallada sobre cómo se produjo la amenaza y qué sistemas se han visto afectados. Microsoft 365 Defender puede realizar una acción automatizada para evitar o detener el ataque.

![image](https://user-images.githubusercontent.com/63270579/194733419-258b13e1-53cd-4e96-a187-a7a6c3a53aff.png)

## Describir Microsoft Defender for Office 365

Microsoft Defender for Office 365 protege su organización frente a amenazas malintencionadas que plantean los mensajes de correo electrónico, los vínculos (URL) y las herramientas de colaboración, incluidos Microsoft Teams, SharePoint Online, OneDrive para la empresa y otros clientes de Office.

![image](https://user-images.githubusercontent.com/63270579/194733452-6abdd4ad-59bd-4235-80c0-ed4460c7858b.png)

Microsoft Defender for Office 365 está disponible en dos planes. El plan que elija influye en las herramientas que verá y usará. Es importante asegurarse de que selecciona el mejor plan para satisfacer las necesidades de su organización.

![image](https://user-images.githubusercontent.com/63270579/194733668-87281958-aad8-42df-bf47-82d5d43a8932.png)



![image](https://user-images.githubusercontent.com/63270579/194733707-4ef43841-ac74-40af-b7f4-3ca9ff0baeaa.png)


![image](https://user-images.githubusercontent.com/63270579/194733724-6c682482-2dd1-41f8-920f-d9fd983afb22.png)


## Microsoft Defender para punto de conexión

![image](https://user-images.githubusercontent.com/63270579/194733816-a50700a0-4766-47e1-9a1e-33cd68a8c1f9.png)

Microsoft Defender para punto de conexión es una plataforma diseñada para ayudar a las redes empresariales a proteger los puntos de conexión. Lo hace mediante la prevención, detección, investigación y respuesta a amenazas avanzadas. Microsoft Defender para punto de conexión incorpora tecnología integrada en los servicios en la nube de Windows 10 y MSFT.

Esta tecnología incluye sensores de comportamiento de punto de conexión que recopilan y procesan señales del sistema operativo, análisis de seguridad en la nube que convierten las señales en información detallada, detecciones y recomendaciones, e información sobre amenazas para identificar herramientas y técnicas de atacantes, y generar alertas.

## Descripción de Microsoft Defender for Cloud Apps

Microsoft Defender for Cloud Apps es un agente de seguridad de acceso a la nube (CASB). Se trata de una solución completa entre SaaS que funciona como intermediario entre un usuario en la nube y el proveedor de la nube. Microsoft Defender for Cloud Apps proporciona una amplia visibilidad a sus servicios en la nube, control sobre el desplazamiento de los datos y análisis sofisticado para identificar y combatir ciberamenazas en todos los servicios en la nube de Microsoft y de terceros. Use este servicio para obtener visibilidad en Shadow IT mediante la detección de las aplicaciones en la nube que se usan. Puede controlar y proteger los datos de las aplicaciones una vez que las autorice para el servicio. 

### Cloud access security broker ( CASB ) un agente ;)

A cloud access security broker, often abbreviated (CASB), is a security policy enforcement point positioned between enterprise users and cloud service providers. CASBs can combine multiple different security policies, from authentication and credential mapping to encryption, malware detection, and more, offering flexible enterprise solutions that help ensure cloud app security across authorized and unauthorized applications, and managed and unmanaged devices

### ¿Qué es un agente de seguridad de acceso a la nube?

Un CASB actúa como un equipo selector para remediar el acceso en tiempo real entre los usuarios empresariales y los recursos en la nube que usan, dondequiera que estén ubicados e independientemente del dispositivo que estén usando. Los CASB ayudan a las organizaciones a proteger su entorno ofreciendo una amplia gama de funcionalidades en los pilares siguientes:

Visibilidad: detección del uso de aplicaciones y servicios en la nube y provisión de visibilidad en Shadow IT.

Protección contra amenazas: supervisión de las actividades del usuario en busca de comportamientos anómalos, control del acceso a los recursos a través de controles de acceso y mitigación del malware.

Seguridad de datos: identificación, clasificación y control de la información confidencial, y protección contra actores malintencionados.

Cumplimiento: evaluación del cumplimiento de los servicios en la nube.

Estas áreas de funcionalidad representan la base del marco Defender for Cloud Apps que se describe a continuación.

### Office 365 Cloud App Security

Cloud App Security de Office 365 es un subconjunto de Microsoft Defender for Cloud Apps que proporciona visibilidad y control mejorados para Office 365. Office 365 Cloud App Security incluye detección de amenazas basada en registros de actividad del usuario, descubrimiento de Shadow IT para aplicaciones con funcionalidad similar a las ofertas de Office 365, control de permisos de aplicaciones para Office 365 y aplicación de controles de acceso y sesión.

### Cloud App Discovery mejorado en Azure Active Directory

Azure Active Directory Premium P1 incluye Azure Active Directory Cloud App Discovery sin coste adicional. Esta característica se basa en las capacidades de Cloud Discovery de Microsoft Defender for Cloud Apps, que proporcionan una mayor visibilidad del uso de aplicaciones en la nube en la organización.

Proporciona un subconjunto reducido de las capacidades de detección de Microsoft Defender for Cloud Apps.

Use Microsoft Defender for Cloud Apps para identificar de forma inteligente y proactiva, y responder a las amenazas de los servicios en la nube de Microsoft y que no sean de Microsoft.

## Microsoft Defender for Identity

Microsoft Defender for Identity es una solución de seguridad basada en la nube. Utiliza sus datos de Active Directory local (llamados señales) para identificar, detectar e investigar amenazas avanzadas, identidades comprometidas y acciones internas malintencionadas dirigidas a su organización.

Microsoft Defender for Identity permite a los profesionales de seguridad administrar la funcionalidad de entornos híbridos para hacer lo siguiente:

Supervisar las actividades y el comportamiento del usuario del perfil.
Proteger las identidades de usuario y reducir la superficie expuesta a ataques.
Identificar e investigar actividades sospechosas y ataques avanzados a lo largo de la cadena de eliminación del ciberataque.
Proporcionar información clara sobre los incidentes en una escala de tiempo sencilla para una rápida evaluación de prioridade

Defender for Identity supervisa y analiza las actividades de los usuarios y la información en su red, incluidos los permisos y la pertenencia a grupos, y crea una línea de base de comportamiento para cada usuario.

Defender for Identity proporciona información sobre las configuraciones de identidades y procedimientos recomendados de seguridad. A través de informes de seguridad y análisis de perfil de usuario, Defender for Identity ayuda a reducir la superficie de ataque de su organización, lo que dificulta comprometer las credenciales de usuario y promover un ataque.

Normalmente, los ataques se lanzan contra cualquier entidad accesible, como un usuario con pocos privilegios. Después, los ataques se mueven rápidamente hasta que el atacante accede a recursos valiosos. Estos recursos pueden incluir cuentas confidenciales, administradores de dominio y datos extremadamente confidenciales. Defender for Identity identifica estas amenazas avanzadas en el origen a lo largo de toda la cadena de eliminación del ciberataque:

Reconocimiento

Credenciales en peligro

Movimientos laterales

Dominación de dominio

## Descripción del portal de Microsoft 365 Defender

Microsoft 365 Defender coordina de forma nativa la detección, la prevención, la investigación y la respuesta a través de los puntos de conexión, las identidades, el correo electrónico y las aplicaciones para proporcionar protección integrada frente a ataques sofisticados. El portal de Microsoft 365 Defender reúne estas funcionalidades en un lugar central diseñado para satisfacer las necesidades de los equipos de seguridad y resalta el acceso rápido a la información con diseños más sencillos. A través del portal de Microsoft 365 Defender puede ver el estado de seguridad de su organización.

Debe tener asignado un rol adecuado, como administrador global, administrador de seguridad, operador de seguridad o lector de seguridad en Azure Active Directory para acceder al portal de Microsoft 365 Defender.


#### Diferencias entre la puntuación de seguridad de Microsoft 365 Defender y Microsoft Defender for Cloud

Existe una puntuación de seguridad de Microsoft 365 Defender y Microsoft Defender for Cloud, pero son ligeramente distintas. La puntuación de seguridad de Microsoft Defender for Cloud es una medida de la posición de seguridad de las suscripciones de Azure. La puntuación de seguridad del portal de Microsoft 365 Defender es una medida de la posición de seguridad de la organización en las aplicaciones, los dispositivos y las identidades.


El acceso a Microsoft 365 Defender se configura con roles globales de Azure Active Directory o mediante roles personalizados.

## Descripción del Portal de confianza de servicios y de la privacidad en Microsoft

El Portal de confianza de servicios proporciona información, herramientas y otros recursos sobre las prácticas de seguridad, privacidad y cumplimiento de Microsoft. Inicie sesión con su cuenta de servicios en la nube de Microsoft para acceder a toda la documentación disponible


![image](https://user-images.githubusercontent.com/63270579/194939214-b554a2c0-b364-4493-91bb-54ab7008cbd1.png)

### Descripción de Microsoft Priva

Microsoft Priva le ayuda a superar estos desafíos para que pueda alcanzar sus objetivos de privacidad. Las funcionalidades de Priva están disponibles mediante dos soluciones: Administración de riesgo de privacidad Priva, que ofrece visibilidad de las plantillas de directivas y datos de la organización para reducir los riesgos, y Solicitudes de derechos de los interesados Priva, que proporciona herramientas de automatización y flujo de trabajo para satisfacer solicitudes de datos.

Microsoft Priva le ayuda a comprender los datos que almacena su organización mediante la detección automática de recursos de datos personales y la visualización de información esencial. Estas visualizaciones se pueden consultar en las páginas de información general y perfil de datos, a las que se puede acceder actualmente mediante el Portal de cumplimiento de Microsoft Purview.

Priva evalúa los datos de la organización almacenados en los siguientes servicios de Microsoft 365 en el inquilino de Microsoft 365:

Exchange Online

SharePoint Online

OneDrive para la Empresa

Microsoft Teams

## Descripción de la protección de la información y la administración del ciclo de vida de los datos en Microsoft Purview ( que tipos de datos tienes )

![image](https://user-images.githubusercontent.com/63270579/194942266-afe75cdc-b552-4eb0-9d02-0f0c296f81d1.png)


Las organizaciones necesitan proteger todo tipo de información, incluida la información financiera y personal. Esto debe hacerse para garantizar que los clientes, empleados y la organización estén protegidos frente a riesgos. La organización debe mantener los estándares de cumplimiento dondequiera que opere.

Microsoft Purview Information Protection detecta, clasifica y protege contenido confidencial y crítico para la empresa durante todo su ciclo de vida en toda la organización. Proporciona las herramientas necesarias para conocer los datos, protegerlos y evitar su pérdida.

La Administración del ciclo de vida de los datos en Microsoft Purview administra el ciclo de vida del contenido mediante soluciones para importar, almacenar y clasificar los datos críticos para la empresa, de modo que puede conservar lo que necesita y eliminar lo que no necesita. Ofrece a las organizaciones la capacidad de controlar sus datos, con fines de cumplimiento normativo.

![image](https://user-images.githubusercontent.com/63270579/194942385-2ef98f60-b26f-48b6-90b9-1a34dc79b7f2.png)

**El Cumplimiento de Microsoft 365 ahora se denomina Microsoft Purview y las soluciones dentro del área de cumplimiento se han cambiado de marca. Para más información sobre Microsoft Purview, vea el anuncio del blog.**

Microsoft Purview incluye muchos tipos de información confidencial basados en patrones definidos por una expresión regular (regex) o una función.

Algunos ejemplos son:

Números de tarjeta de crédito

Números de pasaporte o de identificación

Números de cuentas bancarias

Números de servicios de salud

Los clasificadores que se pueden entrenar utilizan inteligencia artificial y aprendizaje automático para clasificar los datos de forma inteligente. Son especialmente útiles para clasificar datos únicos para una organización, como tipos específicos de contratos, facturas o registros de clientes. Este método de clasificación consiste más en entrenar un clasificador para identificar un elemento en función de lo que el elemento es, no de lo que contiene (coincidencia de patrones). Hay dos tipos de clasificadores disponibles:

####  ¿Qué es el explorador de contenido?

El explorador de contenido está disponible como una pestaña en el panel de clasificación de datos del Portal de cumplimiento. Permite a los administradores obtener visibilidad sobre el contenido que se ha resumido en el panel de información general.

#### ¿Qué es el explorador de actividades?

El explorador de actividades proporciona visibilidad sobre qué contenido se ha detectado y etiquetado, y dónde está. Permite supervisar lo que se está haciendo con el contenido etiquetado en toda la organización. Los administradores obtienen visibilidad de las actividades a nivel de documento, como los cambios y la degradación de etiquetas (por ejemplo, cuando alguien cambia una etiqueta de confidencial a pública).

### Descripción de las directivas y las etiquetas de confidencialidad

El Cumplimiento de Microsoft 365 ahora se denomina Microsoft Purview y las soluciones dentro del área de cumplimiento se han cambiado de marca. Para más información sobre Microsoft Purview, vea el anuncio del blog.

### Descripción de la prevención de la pérdida de datos

La prevención de pérdida de datos (DLP) de Microsoft Purview es una manera de proteger la información confidencial y evitar su divulgación de forma accidental. Con las directivas DLP, los administradores pueden hacer lo siguiente:

![image](https://user-images.githubusercontent.com/63270579/194950360-a8e38b94-a6e8-46e7-8c03-e1ee02521784.png)

Por ejemplo, un administrador puede configurar una directiva DLP que ayude a detectar información sujeta al cumplimiento de una normativa, como la Ley de transferencia y responsabilidad de seguros de salud (HIPAA), en todos los sitios de SharePoint y OneDrive para la Empresa. El administrador puede impedir que los documentos correspondientes se compartan de forma inapropiada.

![image](https://user-images.githubusercontent.com/63270579/194951042-55b0ee77-48d8-4c8f-aec6-1c16c19dc7ca.png)


Las reglas de la directiva se clasifican por orden de prioridad en cuanto a su implementación. Por ejemplo, en el diagrama anterior, la regla uno tiene prioridad sobre la regla dos, etc.

#### Puntos de conexión de servicio de red virtual

El punto de conexión de servicio de red virtual (VNet) proporciona conectividad directa y segura con los servicios de Azure por medio de una ruta optimizada a través de la red troncal de Azure. Los puntos de conexión permiten proteger los recursos de servicio de Azure críticos únicamente para las redes virtuales. Los puntos de conexión de servicio permiten a las direcciones IP privadas de la red virtual alcanzar el punto de conexión de un servicio de Azure sin necesidad de una dirección IP pública en la red virtual.

![image](https://user-images.githubusercontent.com/63270579/194955123-a47df2f8-afcb-49f5-8993-e8c3e34711a5.png)


Las características de prevención de la pérdida de datos se han ampliado a los mensajes de chat y de canal de Microsoft Teams, incluidos los mensajes de canales privados. Con DLP, los administradores ahora pueden definir directivas que impidan que los usuarios compartan información confidencial en un canal o una sesión de chat de Teams, ya sea en un mensaje o en un archivo. Al igual que con Exchange, Outlook, SharePoint y OneDrive para la Empresa, los administradores pueden usar las sugerencias de las directivas DLP que se muestran a los usuarios para explicarles por qué se ha desencadenado una directiva. Por ejemplo, en la captura de pantalla siguiente se muestra una sugerencia de directiva en un mensaje de chat que se ha bloqueado porque el usuario ha intentado compartir un número de la seguridad social de Estados Unidos.

Con las directivas DLP, Microsoft Teams puede ayudar a los usuarios a colaborar de forma segura y en línea con los requisitos de cumplimiento.

## Descripción de las directivas y las etiquetas de retención

Las directivas y las etiquetas de retención ayudan a las organizaciones a administrar y controlar la información, ya que garantizan que el contenido se mantenga únicamente durante el tiempo necesario y, después, se elimine de forma permanente. La aplicación de etiquetas de retención y la asignación de directivas de retención ayuda a las organizaciones

![image](https://user-images.githubusercontent.com/63270579/194955838-f6d21788-0ca3-4d2d-b4c0-520a8c1df33d.png)


### Descripción de la administración de registros

El Cumplimiento de Microsoft 365 ahora se denomina Microsoft Purview y las soluciones dentro del área de cumplimiento se han cambiado de marca. La Administración de registros en Microsoft 365 ahora es la Administración de registros en Microsoft Purview. Para más información sobre Microsoft Purview, vea el anuncio del blog.

![image](https://user-images.githubusercontent.com/63270579/194956931-7c5addbf-1caf-4ad0-82ec-89071e8c9c23.png)



#### Prueba de conocimiento ( conceptos clave que puedes entender) 

![image](https://user-images.githubusercontent.com/63270579/194957734-67ff5526-cff5-4dde-bc3f-6c99f72dd76c.png)

![image](https://user-images.githubusercontent.com/63270579/194957778-098e1bcd-83b1-4783-8577-d946315cb05a.png)

![image](https://user-images.githubusercontent.com/63270579/194957870-e9424943-153e-4c5d-a82b-cb0a64587741.png)

![image](https://user-images.githubusercontent.com/63270579/194957926-77a0237d-cdd2-4ef7-b9c1-5c4964224d47.png)


## Descripción de las capacidades de riesgo interno en Microsoft Purview

La administración y reducción del riesgo en una organización comienza con la comprensión de los tipos de riesgos que se encuentran en el área de trabajo moderna. Algunos riesgos están controlados por eventos y factores externos y están fuera del control directo de una organización. Otros riesgos están impulsados por eventos internos y actividades de empleados que se pueden eliminar y evitar. Algunos ejemplos son los riesgos de acciones y comportamiento ilegales, inadecuados, no autorizados o no éticos por parte de los empleados y los administradores. Estos comportamientos pueden conducir a una amplia gama de riesgos internos de los empleados:

Fugas de datos confidenciales y pérdida de datos

Infracciones de confidencialidad

Robo de propiedad intelectual (IP)

Fraude

Transacciones internas

Infracciones de cumplimiento normativo

![image](https://user-images.githubusercontent.com/63270579/194960014-a5ed58b4-817c-4061-a74b-d339012dbf3d.png)


La administración de riesgos internos puede ayudarle a detectar, investigar y tomar medidas para mitigar los riesgos internos de la organización en varios escenarios comunes. Estos escenarios incluyen el robo de datos por parte de los empleados, la fuga intencional o accidental de información confidencial, el comportamiento ofensivo, etc. 


### Descripción del cumplimiento de comunicaciones

El Cumplimiento de comunicaciones en el Portal de cumplimiento de Microsoft Purview ayuda a minimizar los riesgos de comunicación, ya que permite a las organizaciones detectar, capturar y realizar acciones de corrección para mensajes inadecuados. Las directivas predefinidas y personalizadas en el cumplimiento de comunicaciones permiten examinar las comunicaciones internas y externas de las coincidencias de directivas para que puedan examinarlas los revisores elegidos.

La identificación y resolución de problemas de compatibilidad con el Cumplimiento de comunicaciones en Microsoft Purview utiliza el siguiente flujo de trabajo:

El cumplimiento de comunicaciones permite a los revisores investigar correos electrónicos examinados y mensajes en Microsoft Teams, Exchange Online, Yammer o comunicaciones de terceros en una organización, con las acciones de corrección adecuadas para asegurarse de que cumplen con los estándares de mensajes de la organización.

### Descripción de las barreras de información

La característica de Barreras de información en Microsoft Purview se admite en Microsoft Teams, SharePoint Online y OneDrive para la Empresa.

Las barreras de la información son directivas que los administradores pueden configurar para impedir que personas o grupos se comuniquen entre sí. Cuando se aplican directivas de barrera de información, las personas que no deben comunicarse con otros usuarios específicos no pueden encontrar ni seleccionar esos usuarios, así como tampoco chatear con ellos ni llamarlos. Con las barreras de información, las comprobaciones están en vigor para evitar la comunicación no autorizada.

![image](https://user-images.githubusercontent.com/63270579/194960977-af664f03-1351-4671-84bf-6cd99d6aa520.png)

![image](https://user-images.githubusercontent.com/63270579/194961042-9ca05576-9067-4dbe-ac12-21d036aa96c2.png)

### Descripción de las funcionalidades de eDiscovery y de auditoría de Microsoft Purview


Es posible que las organizaciones necesiten identificar, recopilar o auditar información por motivos legales, normativos o empresariales. Obtenga información sobre cómo las funcionalidades de eDiscovery y de auditoría de Microsoft Purview ayudan a las organizaciones a encontrar datos pertinentes rápidamente.

> El Cumplimiento de Microsoft 365 ahora se denomina Microsoft Purview y las soluciones dentro del área de cumplimiento se han cambiado de marca. Core eDiscovery en Office 365 ahora es eDiscovery (Estándar) en Microsoft Purview. eDiscovery avanzado en Office 365 ahora es eDiscovery (Premium) en Microsoft Purview.

La exhibición de documentos electrónicos, o eDiscovery, es el proceso de identificación y entrega de información electrónica que se puede utilizar como prueba en casos legales. Puede usar herramientas de eDiscovery en Microsoft Purview para buscar contenido en Exchange Online, OneDrive para la Empresa, SharePoint Online, Microsoft Teams, Grupos de Microsoft 365 y equipos de Yammer. Puede buscar buzones y sitios en la misma búsqueda de eDiscovery y, a continuación, exportar los resultados de la búsqueda. Puede usar los casos de eDiscovery para identificar, suspender y exportar el contenido que haya encontrado en los buzones y sitios.

![image](https://user-images.githubusercontent.com/63270579/195144561-844fa841-dfa2-4591-bd0d-4e940a4c1c88.png)

Las soluciones de auditoría de Microsoft Purview ayudan a las organizaciones a responder eficazmente a eventos de seguridad, investigaciones forenses, investigaciones internas y obligaciones de cumplimiento. Miles de operaciones de usuario y administrador realizadas en docenas de servicios y soluciones de Microsoft 365 se capturan, registran y conservan en el registro de auditoría unificado de su organización. Los operadores de seguridad, administradores de TI, equipos de riesgo interno e investigadores legales y de cumplimiento de su organización pueden buscar en los registros de auditoría de estos eventos. Esta funcionalidad proporciona visibilidad de las actividades realizadas en toda la organización en Microsoft 365.

Microsoft Purview proporciona dos soluciones de auditoría: Auditoría (Estándar) y Auditoría (Premium).


![image](https://user-images.githubusercontent.com/63270579/195145871-b2428f16-e867-4d29-82e9-1736eb88aef7.png)


![image](https://user-images.githubusercontent.com/63270579/195145954-83bd0443-e9dc-4b89-a25e-b22f379cea52.png)


## Descripción de las funcionalidades de la gobernanza de recursos en Azure

### Descripción de Azure Policy

Azure Policy evalúa todos los recursos de Azure y los recursos habilitados para Arc (tipos de recursos específicos hospedados fuera de Azure).

Azure Policy evalúa si las propiedades de los recursos coinciden con las reglas de negocio. Estas reglas de negocio se describen mediante el formato JSON y se conocen como definiciones de directiva. Para una administración simplificada, puede agrupar varias reglas de negocio para formar una única iniciativa de directiva. Una vez formadas las reglas de negocio, puede asignar la definición o la iniciativa de directiva a cualquier ámbito de recursos admitidos, como grupos de administración, suscripciones, grupos de recursos o recursos individuales.

## ¿Cuál es la diferencia entre Azure Policy y el control de acceso basado en roles (RBAC) de Azure?

Es importante no confundir Azure Policy y Azure RBAC. Use Azure Policy para asegurarse de que el estado del recurso sea compatible con las reglas de negocio de su organización, independientemente de quién haya realizado el cambio o de quién tenga permiso para realizar cambios. Azure Policy evaluará el estado de un recurso y actuará para asegurarse de que el recurso siga siendo compatible.

Azure RBAC, en cambio, se centra en la administración de las acciones del usuario en ámbitos diferentes. Azure RBAC administra quién tiene acceso a los recursos de Azure, qué se puede hacer con esos recursos y a qué áreas se puede acceder. Si es necesario controlar las acciones, se usaría Azure RBAC. Si una persona tiene acceso para realizar una acción, pero el resultado es un recurso no compatible, Azure Policy todavía bloqueará la acción.

Azure RBAC y Azure Policy deben usarse conjuntamente para lograr un control total del ámbito en Azure

## Descripción del uso de Azure Blueprints

Azure Blueprints proporciona una manera de definir un conjunto repetible de recursos de Azure. Azure Blueprints permite a los equipos de desarrollo aprovisionar y ejecutar rápidamente nuevos entornos, a sabiendas de que cumplen los requisitos de cumplimiento de la organización. Los equipos también pueden aprovisionar recursos de Azure en varias suscripciones simultáneamente, lo que significa que pueden lograr tiempos de desarrollo más cortos y una entrega más rápida.

Azure Blueprints ayuda a garantizar que los recursos de Azure se implementan según los requisitos de cumplimiento. Sin embargo, se debe usar un servicio como Azure Policy para supervisar continuamente los recursos y garantizar una continuidad de los requisitos de cumplimiento.

## Describir las funcionalidades en el portal de gobernanza de Microsoft Purview

Microsoft Purview está diseñado para abordar los desafíos asociados al rápido crecimiento de los datos y para ayudar a las empresas a sacar el máximo partido de los recursos de información.

El portal de gobernanza de Microsoft Purview es un servicio unificado de gobernanza de datos que le ayuda a administrar los datos locales, de varias nubes y de software como servicio (SaaS). El portal de gobernanza de Microsoft Purview le permite realizar las siguientes acciones:

Cree un mapa holístico actualizado del panorama de sus datos con detección automatizada de datos, clasificación de datos confidenciales y linaje de datos de principio a fin.
Habilite los conservadores de datos para administrar y proteger su patrimonio de datos.
Permita a los consumidores de datos encontrar datos valiosos y confiables.

![image](https://user-images.githubusercontent.com/63270579/195148581-5a415e30-76a5-4b24-b6de-226e0df83432.png)


![image](https://user-images.githubusercontent.com/63270579/195148636-899aa6e3-11bd-47c3-b8be-0bfc77fddce3.png)


La tarjeta Administrador de cumplimiento. Esta tarjeta le lleva a la solución Administrador de cumplimiento de Microsoft Purview. El Administrador de cumplimiento ayuda a simplificar la forma de administrar el cumplimiento. Calcula una puntuación de cumplimiento basada en riesgos que mide el progreso para completar las acciones recomendadas a fin de reducir los riesgos asociados con la protección de datos y los estándares normativos. La solución Administrador de cumplimiento también proporciona funcionalidades de flujo de trabajo y asignación de controles integrada para ayudarle a llevar a cabo de forma eficaz acciones de mejora.

La tarjeta Catálogo de soluciones se vincula a colecciones de soluciones integradas que facilitan la administración de escenarios de cumplimiento de un extremo a otro. Entre las áreas de soluciones se incluyen las siguientes:

Protección y gobernanza de la información. Estas soluciones ayudan a las organizaciones a clasificar, proteger y conservar los datos donde residen y dondequiera que vayan. Se incluyen la administración del ciclo de vida de los datos, la prevención de pérdida de datos, la protección de la información y la administración de registros.
Privacidad. Cree un entorno de trabajo más resistente a la privacidad. La administración de privacidad proporciona conclusiones prácticas sobre los datos personales de la organización para ayudarle a detectar problemas y reducir los riesgos.
Administración de riesgos internos. Estas soluciones ayudan a las organizaciones a identificar, analizar y corregir los riesgos internos antes de que causen daños. Se incluyen el cumplimiento de comunicaciones, las barreras de información y la administración de riesgos internos.
Detección y respuesta. Estas soluciones ayudan a las organizaciones a encontrar, investigar y responder rápidamente con los datos pertinentes. Se incluyen auditorías, solicitudes de interesados y eDiscovery.

## Descripción del Administrador de cumplimiento

El Administrador de cumplimiento de Microsoft Purview es una característica del Portal de cumplimiento de Microsoft Purview que ayuda a los administradores a administrar los requisitos de cumplimiento de una organización con mayor facilidad y comodidad. El Administrador de cumplimiento ayuda a las organizaciones a lo largo del recorrido del cumplimiento; por ejemplo, la creación del inventario de los riesgos de protección de datos, la administración de las complejidades de la implementación de controles, la actualización de las regulaciones y las certificaciones y la generación de informes para los auditores.

Controles
Un control es un requisito de un reglamento, un estándar o una directiva. Define cómo evaluar y administrar la configuración del sistema, el proceso de la organización y las personas responsables de cumplir el requisito específico de un reglamento, un estándar o una directiva.

El Administrador de cumplimiento realiza un seguimiento de los siguientes tipos de controles:

## Controles administrados por Microsoft:

son controles para los Servicios en la nube de Microsoft; asimismo, Microsoft es responsable de implementarlos.
Sus controles: a veces se denominan "controles administrados por el cliente" y se implementan y administran en la organización.
Controles compartidos: la organización y Microsoft comparten la responsabilidad de implementar estos controles.
Compliance Manager evalúa continuamente los controles mediante el examen del entorno de Microsoft 365 y la detección de la configuración del sistema, actualizando continua y automáticamente el estado técnico de la acción.

## Valoraciones

Una valoración es una agrupación de controles de una directiva, una norma o un reglamento específicos. Si completa las acciones de una valoración, cumplirá los requisitos de un estándar, un reglamento o una ley. Por ejemplo, es posible que una organización tenga una valoración que, al completarse, equipare su configuración de Microsoft 365 con los requisitos de la norma ISO 27001.

Una valoración consta de varios componentes, incluidos los servicios que están dentro del ámbito, los controles y una puntuación de valoración que muestra el progreso para completar las acciones necesarias para el cumplimiento.

## Plantillas

El Administrador de cumplimiento proporciona plantillas para que los administradores puedan crear valoraciones rápidamente. Igualmente, pueden modificar estas plantillas para crear una valoración optimizada para sus necesidades. Los administradores también pueden crear una valoración personalizada mediante la creación de una plantilla con sus propias acciones y controles. Por ejemplo, es posible que el administrador quiera crear una plantilla que abarque un control interno del proceso empresarial o un estándar de protección de datos regional que no esté incluido en una de las más de 150 plantillas de valoración generadas previamente de Microsoft.


## Acciones de mejora

Las acciones de mejora le permiten centralizar las actividades de cumplimiento. Cada acción de mejora proporciona instrucciones recomendadas para que las organizaciones puedan cumplir los estándares y las regulaciones de protección de datos. Asimismo, las acciones de mejora se pueden asignar a los usuarios de la organización para que realicen trabajos de implementación y pruebas. Los administradores también pueden almacenar la documentación, las notas y las actualizaciones de estado del Registro en la acción de mejora

## Descripción del uso y las ventajas de la puntuación de cumplimiento

La puntuación de cumplimiento mide el progreso según la realización de las acciones de mejora recomendadas en los controles. Asimismo, la puntuación permite que una organización comprenda su postura de cumplimiento actual. También permite que la organización clasifique por orden de prioridad las acciones en función de su potencial para reducir el riesgo.

Los administradores pueden obtener un desglose de la puntuación de cumplimiento en el panel de información general del Administrador de cumplimiento.

## ¿Cuál es la diferencia entre el Administrador de cumplimiento y la puntuación de cumplimiento?

El Administrador de cumplimiento es una solución completa en el Portal de cumplimiento de Microsoft Purview, que permite que los administradores administren y realicen un seguimiento de las actividades de cumplimiento. En cambio, la puntuación de cumplimiento es un cálculo de la posición de cumplimiento general en toda la organización. La puntuación de cumplimiento está disponible a través del Administrador de cumplimiento.

El Administrador de cumplimiento ofrece a los administradores las funciones que necesitan para comprender y aumentar su puntuación de cumplimiento, de modo que puedan mejorar en última instancia la posición de cumplimiento de la organización y que así pueda lograr los requisitos de cumplimiento.

![image](https://user-images.githubusercontent.com/63270579/195698261-d87364cf-578a-4293-b592-1f8eb717c387.png)

![image](https://user-images.githubusercontent.com/63270579/195698336-7f15f5b7-e009-4555-bfe7-a40cae4a776d.png)


# Estudio 

## Describe the capabilities in the Microsoft Purview governance portal

Microsoft Purview's solutions in the governance portal provide a unified data governance service that helps you manage your on-premises, multicloud, and software-as-a-service (SaaS) data. The Microsoft Purview governance portal allows you to:

Create a holistic, up-to-date map of your data landscape with automated data discovery, sensitive data classification, and end-to-end data lineage.
Enable data curators to manage and secure your data estate.
Empower data consumers to find valuable, trustworthy data.

Microsoft Purview automatiza el descubrimiento de datos proporcionando análisis y clasificación de datos como un servicio para activos en todo su patrimonio de datos. Los metadatos y las descripciones de los activos de datos descubiertos se integran en un mapa holístico de su patrimonio de datos. Encima de este mapa, hay aplicaciones especialmente diseñadas que crean entornos para el descubrimiento de datos, la administración de acceso y la información sobre su panorama de datos.


![image](https://user-images.githubusercontent.com/63270579/197583145-c993e3ca-d2ae-44dd-a98f-0dd04b4cc226.png)

![image](https://user-images.githubusercontent.com/63270579/197585337-db421a1b-17e0-4aa5-a7c6-b0cd5b839cb6.png)


## Describe Azure Blueprints 

 Azure Blueprints permite a los arquitectos de la nube y a los grupos centrales de tecnología de la información definir un conjunto repetible de recursos de Azure que implementa y se adhiere a los estándares, patrones y requisitos de una organización. Azure Blueprints hace posible que los equipos de desarrollo construyan y pongan en marcha rápidamente nuevos entornos con la confianza que están creando dentro del cumplimiento de la organización con un conjunto de componentes integrados, como redes, para acelerar el desarrollo y la entrega.
 
 Los blueprints son una forma declarativa de orquestar la implementación de varias plantillas de recursos y otros artefactos como:

Asignaciones de funciones
Asignaciones de políticas
Plantillas de Azure Resource Manager (plantillas ARM)
Grupos de recursos

### Azure Cosmos DB ( NOSQL, Serverless)

Azure Cosmos DB es una base de datos NoSQL completamente administrada para el desarrollo de aplicaciones modernas. Los tiempos de respuesta de milisegundos de un solo dígito y la escalabilidad automática e instantánea garantizan la velocidad a cualquier escala. La continuidad del negocio está asegurada con disponibilidad respaldada por SLA y seguridad de nivel empresarial.

Como un servicio completamente administrado, Azure Cosmos DB le quita la administración de la base de datos con la administración automática, las actualizaciones y la aplicación de parches. También gestiona la gestión de la capacidad con opciones rentables de escalado automático y sin servidor que responden a las necesidades de las aplicaciones para hacer coincidir la capacidad con la demanda.
 
 El servicio está diseñado para ayudar con la configuración del entorno . Esta configuración a menudo consta de un conjunto de grupos de recursos, políticas, asignaciones de roles e implementaciones de plantillas ARM. Un blueprint es un paquete que reúne cada uno de estos tipos de artefactos y le permite componer y crear versiones de ese paquete, incluso a través de una canalización de integración continua y entrega continua (CI/CD). En última instancia, cada uno se asigna a una suscripción en una sola operación que se puede auditar y rastrear.
 
 ##  Azure Policy 
 
 Azure Policy evaluates resources in Azure by comparing the properties of those resources to business rules. These business rules, described in JSON format, are known as policy definitions. To simplify management, several business rules can be grouped together to form a policy initiative (sometimes called a policySet)
 
 ## Azure Policy Vs Azure RBAC ( role-based access control (Azure RBAC))
 
There are a few key differences between Azure Policy and Azure role-based access control (Azure RBAC). Azure Policy evaluates state by examining properties on resources that are represented in Resource Manager and properties of some Resource Providers. Azure Policy doesn't restrict actions (also called operations). Azure Policy ensures that resource state is compliant to your business rules without concern for who made the change or who has permission to make a change. Some Azure Policy resources, such as policy definitions, initiative definitions, and assignments, are visible to all users. This design enables transparency to all users and services for what policy rules are set in their environment.

Azure RBAC focuses on managing user actions at different scopes. If control of an action is required, then Azure RBAC is the correct tool to use. Even if an individual has access to perform an action, if the result is a non-compliant resource, Azure Policy still blocks the create or update.

The combination of Azure RBAC and Azure Policy provides full scope control in Azure.
 
 ## Get started with information barriers
 
 Information barriers (Chinese Walls) are established organizational arrangements which are designed to prevent the flow of information between separate departments. They are used by legal practices to rebut the presumption of imputed knowledge.
 
 ## Learn about communication compliance
 
 Microsoft Purview Communication Compliance es una solución de riesgo interno que ayuda a minimizar los riesgos de comunicación al ayudarlo a detectar, capturar y actuar sobre mensajes inapropiados en su organización. Las políticas predefinidas y personalizadas le permiten escanear comunicaciones internas y externas en busca de coincidencias de políticas para que puedan ser examinadas por revisores designados. Los revisores pueden investigar el correo electrónico escaneado, los equipos de Microsoft, Yammer o las comunicaciones de terceros en su organización y tomar las medidas adecuadas para asegurarse de que cumplen con los estándares de mensajes de su organización.
 
 ## Learn about insider risk management
 
 Microsoft Purview Insider Risk Management es una solución de cumplimiento que ayuda a minimizar los riesgos internos al permitirle detectar, investigar y actuar sobre actividades maliciosas e inadvertidas en su organización. Las políticas de riesgo de Insider le permiten definir los tipos de riesgos para identificar y detectar en su organización, lo que incluye actuar en casos y escalar casos a Microsoft eDiscovery (Premium) si es necesario. Los analistas de riesgos de su organización pueden tomar rápidamente las medidas adecuadas para asegurarse de que los usuarios cumplan con los estándares de cumplimiento de su organización.
 
 ### Puntos débiles de riesgo modernos
 
 ![image](https://user-images.githubusercontent.com/63270579/197597877-45c07de1-b826-4e28-9eda-b0b619f7ab2a.png)

 ![image](https://user-images.githubusercontent.com/63270579/197597969-9a78f402-c031-4393-8849-45941581e2b3.png)

## Learn about retention policies and retention labels

Para la mayoría de las organizaciones, el volumen y la complejidad de sus datos aumentan a diario: correo electrónico, documentos, mensajes instantáneos y más. Administrar o gobernar de manera efectiva esta información es importante porque necesita:

retener contenido	Evite la eliminación permanente y permanezca disponible para eDiscovery
Eliminar contenido	Elimine permanentemente el contenido de su organización

![image](https://user-images.githubusercontent.com/63270579/197599076-8031989f-a52d-471a-b956-4041d74dbc14.png)


Use una política de retención para asignar la misma configuración de retención para el contenido a nivel de sitio o buzón, y use una etiqueta de retención para asignar configuraciones de retención a nivel de elemento (carpeta, documento, correo electrónico).

![image](https://user-images.githubusercontent.com/63270579/197599319-f514ed51-0be8-4805-aff2-2dc4ab618265.png)


***prevención de pérdida de datos (DLP)***
 
 ![image](https://user-images.githubusercontent.com/63270579/197599604-e1b2ee5a-9769-4515-87d7-a82fa960fec1.png)


## Describe Records Management

Un sistema de gestión de registros, también conocido como gestión de registros e información, es una solución para que las organizaciones administren registros reglamentarios, legales y críticos para el negocio. La administración de registros para Microsoft Purview lo ayuda a cumplir con las obligaciones legales de su organización, brinda la capacidad de demostrar el cumplimiento de las reglamentaciones y aumenta la eficiencia con la disposición regular de elementos que ya no es necesario conservar, que ya no tienen valor o que ya no se requieren para el negocio. propósitos

![image](https://user-images.githubusercontent.com/63270579/197601127-f19bb0a2-62d1-43ca-8290-2255d5fcfee8.png)

## Describe Data Loss Prevention (DLP)

 Las políticas que definen cómo se pueden compartir los datos se conocen como políticas de prevención de pérdida de datos (DLP).

Para obtener más información sobre cómo proteger sus datos, consulte Políticas de prevención de pérdida de datos en la guía de administración de ***Microsoft Power Platform***

## Describe sensitivity labels


Las etiquetas de confidencialidad de *** Microsoft Purview Information Protection*** le permiten clasificar y proteger los datos de su organización, mientras se asegura de que la productividad del usuario y su capacidad para colaborar no se vean obstaculizadas.

## Get started with activity explorer

La descripción general de la clasificación de datos y las pestañas del explorador de contenido le brindan visibilidad sobre qué contenido se ha descubierto y etiquetado, y dónde está ese contenido. El Explorador de actividades completa este conjunto de funcionalidades al permitirle monitorear lo que se está haciendo con su contenido etiquetado. El Explorador de actividades proporciona una vista histórica de las actividades en su contenido etiquetado. La información de la actividad se recopila de los registros de auditoría unificados de Microsoft 365, se transforma y está disponible en la interfaz de usuario del explorador de actividades. El explorador de actividad informa sobre datos de hasta 30 días.


![image](https://user-images.githubusercontent.com/63270579/197603083-bd22b0d5-1ade-4e71-b97e-5b646da5ec2b.png)


## How to use the Microsoft data classification dashboard ( In the Microsoft Pureview compliance portal) 

As a Microsoft 365 administrator or compliance administrator, you can evaluate and then tag content in your organization in order to control where it goes, protect it no matter where it is, and ensure that it is preserved and deleted according to your organization's needs. You do this through the application of sensitivity labels, retention labels, and sensitive information type classification. There are various ways to do the discovery, evaluation, and tagging, but the end result is that you may have very large numbers of documents and emails that are tagged and classified with one or both of these labels. After you apply your retention labels and sensitivity labels, you'll want to see how the labels are being used across your tenant and what is being done with those items. The data classification page provides visibility into that body of content, specifically.

## Compliance score calculation

Compliance Manager calculates a compliance score for your organization. This article explains how to interpret your score, what the Data Protection Baseline assessment includes, continuous monitoring, and how different types of actions are managed and scored.

The Compliance Manager dashboard displays your overall compliance score. This score measures your progress in completing recommended improvement actions within controls. Your score can help you understand your current compliance posture. It can also help you prioritize actions based on their potential to reduce risk.

## Microsoft Purview Compliance Manager

Microsoft Purview Compliance Manager is a feature in the Microsoft Purview compliance portal that helps you manage your organization’s multicloud compliance requirements with greater ease and convenience. Compliance Manager can help you throughout your compliance journey, from taking inventory of your data protection risks to managing the complexities of implementing controls, staying current with regulations and certifications, and reporting to auditors.

The Compliance Manager overview page shows your current compliance score, helps you see what needs attention, and guides you to key improvement actions. Below is an example of the overview page:


![image](https://user-images.githubusercontent.com/63270579/197610079-c871d900-657d-40fb-be7b-ce446b04c554.png)


# Microsoft’s Service Trust Portal and privacy principles

The Microsoft Service Trust Portal provides a variety of content, tools, and other resources about how Microsoft cloud services protect your data, and how you can manage cloud data security and compliance for your organization.

The Service Trust Portal is Microsoft's public site for publishing audit reports and other compliance-related information associated with Microsoft’s cloud services. STP users can download audit reports produced by external auditors and gain insight from Microsoft-authored whitepapers that provide details on how Microsoft cloud services protect your data, and how you can manage cloud data security and compliance for your organization. To access some of the resources on the Service Trust Portal, you must log in as an authenticated user with your Microsoft cloud services account (Azure Active Directory organization account) and review and accept the Microsoft Non-Disclosure Agreement for Compliance Materials.

# Microsoft 365 Defender

Microsoft 365 Defender es un paquete de defensa empresarial unificado previo y posterior a la infracción que coordina de forma nativa la detección, prevención, investigación y respuesta en puntos finales, identidades, correo electrónico y aplicaciones para brindar protección integrada contra ataques sofisticados.

Con la solución integrada Microsoft 365 Defender, los profesionales de la seguridad pueden unir las señales de amenazas que recibe cada uno de estos productos y determinar el alcance y el impacto total de la amenaza; cómo ingresó al entorno, qué se vio afectado y cómo está afectando actualmente a la organización. Microsoft 365 Defender toma medidas automáticas para evitar o detener el ataque y reparar automáticamente los buzones de correo, los puntos de conexión y las identidades de los usuarios afectado

![image](https://user-images.githubusercontent.com/63270579/198065386-b5617e28-6d54-4d2d-acd5-e3f339986107.png)

## Microsoft Defender for Office 365 service description

Microsoft Defender for Office 365 is a cloud-based email filtering service that helps protect your organization against advanced threats to email and collaboration tools, like phishing, business email compromise, and malware attacks. Defender for Office 365 also provides investigation, hunting, and remediation capabilities to help security teams efficiently identify, prioritize, investigate, and respond to threats.

## Microsoft Defender for Endpoint

**Microsoft Defender for Endpoint is an enterprise endpoint security platform designed to help enterprise networks prevent, detect, investigate, and respond to advanced threats.**

## Microsoft Defender for Cloud Apps ( agente Cloud Access Security Broker)

This is where a Cloud Access Security Broker steps in to address the balance, adding safeguards to your organization's use of cloud services by enforcing your enterprise security policies. As the name suggests, CASBs act as a gatekeeper to broker access in real time between your enterprise users and cloud resources they use, wherever your users are located and regardless of the device they are using.


## Microsoft Defender for Identity

Microsoft Defender for Identity (formerly Azure Advanced Threat Protection, also known as Azure ATP) is a cloud-based security solution that leverages your on-premises Active Directory signals to identify, detect, and investigate advanced threats, compromised identities, and malicious insider actions directed at your organization.


## Microsoft 365 Defender portal ( ES DONDE SE ALOJAN LAS ANTERIORES )

The Microsoft 365 Defender portal combines protection, detection, investigation, and response to email, collaboration, identity, device, and cloud app threats, in a central place. The Microsoft 365 Defender portal emphasizes quick access to information, simpler layouts, and bringing related information together for easier use. It includes:


# Describe security capabilities of Microsoft Sentinel

## Microsoft Sentinel a scalable, cloud-native, security information event management (SIEM) and security orchestration automated response (SOAR) solution


# Describe security management capabilities of Azure

## Describe Cloud security posture management (CSPM)

Cloud security posture management (CSPM) is a category of automated data security solution that manages monitoring, identification, alerting, and remediation of compliance risks and misconfigurations in cloud environments.

## Describe Microsoft Defender for Cloud (CWPP Cloud Workload Protection Platform ) ( CSPM (Cloud Security Posture Management ) 

Microsoft Defender for Cloud es un recurso de administración de la posición de seguridad en la nube (CSPM) y la plataforma de protección de cargas de trabajo en la nube (CWPP) para todos los recursos de Azure, locales y multinube (Amazon AWS y Google GCP). Defender for Cloud cubre tres necesidades vitales a medida que administra la seguridad de los recursos y las cargas de trabajo en la nube y en el entorno local.

## Describe security baselines for Azure

Security baselines are standardized documents for Azure product offerings, describing the available security capabilities and the optimal security configurations to help you strengthen security through improved tooling, tracking, and security features



# Estudio 


## Azure Type of identities

Existen varios tipos de identidades en azure de las que destacan ***users, service principals, managed identities, and devices***


### User

A user identity is a representation of something that's managed by Azure AD. Employees and guests are represented as users in Azure AD.

### Service principal

A service principal is, essentially, an identity for an application.

### Managed identity

Managed identities are a type of service principal that are automatically managed in Azure AD and eliminate the need for developers to manage credentials. Managed identities provide an identity for applications to use when connecting to Azure resources that support Azure AD authentication and can be used without any extra cost.

System-assigned se asignan a un recurso y se borran automaticamente cuanod se borra el recurso

User-assigned se aplica a varios recursos no solo uno!

ASDFGHJKL22331

### Device

A device is a piece of hardware, such as mobile devices, laptops, servers, or printers. A device identity gives administrators information they can use when making access or configuration decisions. Device identities can be set up in different ways in Azure AD.

### Tipos ( Muy probable pregunta de examen)

#### Azure AD registered devices

Son pues los normales lo que estan conectados a un dominio ( The goal of Azure AD registered devices is to provide users with support for bring your own device)}


#### Azure AD joined

An Azure AD joined device is a device joined to Azure AD through an organizational account, which is then used to sign in to the device. Azure AD joined devices are generally owned by the organization.

#### Hybrid Azure AD joined devices

Organizations with existing on-premises Active Directory implementations can benefit from the functionality provided by Azure AD by implementing hybrid Azure AD joined devices. These devices are joined to your on-premises Active Directory and Azure AD requiring organizational account to sign in to the device

## concept of external identity

Cuando inicias sesion con google o facebook o incluso los usuarios externos podrian iniciar sesion con sus cuentas empresariales.

## concept of hybrid identity

Muchas organizaciones son una combinación de aplicaciones locales y en la nube entonces para estos casos se pueden usar 3 metdos de autenticacion 

### Azure AD Password hash synchronization

Es el normal el NMTL (supongo pero) pero el hash se verifica osea que lo compara en la nube lo que hace que sea high hability

> This enables user authentication to take place against Azure AD rather than against the organization's own Active Directory instance. A benefit of this approach is that password hash synchronization provides highly available cloud authentication. On-premise users can authenticate with Azure AD to access cloud-based applications, even if the on-premise Active Directory goes down.

### Azure AD pass-through authentication.

Este es alrrevez la comparacion se hace on premises y con ayuda de un agente

> pass-through authentication validates users' passwords directly against your on-premises Active Directory. Password validation doesn't happen in the cloud. This can be an important factor for organizations wanting to enforce their on-premises Active Directory security and password policies.

### Federated authentication.

La federación se recomienda como autenticación para las organizaciones que tienen características avanzadas que actualmente no son compatibles con Azure AD, incluido el inicio de sesión con tarjetas inteligentes o certificados, el inicio de sesión con el servidor de autenticación multifactor (MFA) local y el inicio de sesión con una solución de autenticación de terceros.
 
 # Azure AD roles and role-based access control
 
 Azure AD roles control permissions to manage Azure AD resources. For example, allowing user accounts to be created, or billing information to be viewed. Azure AD supports built-in and custom roles.

Managing access using roles is known as role-based access control (RBAC). Azure AD built-in and custom roles are a form of RBAC in that Azure AD roles control access to Azure AD resources. This is referred to as Azure AD RBAC.

## Difference between Azure AD RBAC and Azure RBAC

Azure AD RBAC - Azure AD roles control access to Azure AD resources such as users, groups, and applications.
Azure RBAC - Azure roles control access to Azure resources such as virtual machines or storage using Azure Resource Management.


# Privileged access lifecycle

Monitoring privileged access is a key part of identity governance.Azure AD Privileged Identity Management (PIM) provides extra controls tailored to securing access rights. PIM helps you minimize the number of people who have access to resources across Azure AD

## Azure AD access reviews

Azure Active Directory (AD) access reviews enable organizations to efficiently manage group memberships, access to enterprise applications, and role assignment.

## Azure Privileged Identity Management (PIM)

that enables you to manage, control, and monitor access to important resources in your organization.PIM reduces the chance of a malicious actor getting access by minimizing the number of people who have access to secure information or resources. By time-limiting authorized users

## Azure Identity Protection ( portal )

Herramienta para detectar identity risk 

> Identity Protection is a tool that allows organizations to accomplish three key tasks:
Automate the detection and remediation of identity-based risks.
Investigate risks using data in the portal.
Export risk detection data to third-party utilities for further analysis.

