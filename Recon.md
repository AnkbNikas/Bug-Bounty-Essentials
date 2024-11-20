# Recon 💻

## Nmap:

- Nmap (Network Mapper) is an essential tool in the bug bounty world for several reasons:

1. Host Discovery: Nmap allows you to identify active devices on a network, which is crucial for mapping the target environment.

2. Port Scanning: You can scan open ports on a host to identify services and applications that might be vulnerable.

3. Version Detection: Nmap can determine the versions of services running on open ports, which helps in identifying specific vulnerabilities.

4. Operating System Fingerprinting: Nmap can guess the operating system of the target host, providing additional information that can be useful for finding vulnerabilities.

5. Custom Scripts: Using the Nmap Scripting Engine (NSE), you can run custom scripts to detect specific vulnerabilities and automate security tasks. These capabilities make Nmap a powerful tool for security researchers looking to identify and exploit vulnerabilities in bug bounty programs.

Legal Issues | Nmap Network Scanning

https://nmap.org/book/legal-issues.html

nmap -A -F -T1 10.10.10.223 -v

-A: Enables all detection options, including service versions, scripts, and more. 

-F: Performs a fast scan of the most common ports (100 by default). 

-T1: Sets the scan speed to "slow," which can be useful to avoid detection. 

-v: Increases the verbosity of the command, providing more information about the scan.


## Ffuf:

- FFUF (Fuzz Faster U Fool) is a fuzzing tool used in bug bounty programs to find vulnerabilities in web applications. Here’s how it can be useful:

1. Directory and File Fuzzing: FFUF can search for hidden directories and files in a web application, helping to identify potential entry points for attacks.

2. Input Injection Testing: By sending a large number of random inputs to the application, FFUF can detect input validation issues and other security errors.

3. Fast and Flexible Scanning: FFUF is quick and allows you to specify inputs and parameters for requests, making it easier to detect specific vulnerabilities.

4. Response Analysis: FFUF analyzes server responses to identify unusual behaviors or errors that might indicate a vulnerability.

5. Using FFUF in a bug bounty program allows you to discover vulnerabilities that might have gone unnoticed with other testing methods, thus improving the application's security.

ffuf -w /usr/share/wordlists/dirb/common.txt -u http://tenet.htb/FUZZ -p 1

SecLists

https://github.com/danielmiessler/SecLists


## Shodan:

- Shodan is a powerful tool for bug bounty programs because it allows for efficient network reconnaissance. Here's how it can be useful:

1. Search for Exposed Services: Shodan lets you search for devices and services exposed on the Internet, such as web servers, open ports, IoT devices, etc.

2. Vulnerability Identification: By finding exposed devices and services, you can analyze if they have known vulnerabilities that could be exploited.

3. Infrastructure Mapping: It helps map an organization's infrastructure, identifying hosts and services that could be potential targets.

4. Misconfiguration Detection: You can find devices with misconfigurations or insecure settings that could be exploited.

5. Search Automation: With Shodan, you can automate searches using specific queries to quickly find vulnerable hosts.

6. Using Shodan in a bug bounty program allows you to identify and prioritize potential targets, improving your chances of finding significant vulnerabilities.

- (Get API key from Web/Account)

- Terminal:

- shodan init (API key)

- shodan info (Credits available in the account)

- shodan -h (Help)

- shodan count wordpress 1.4.7 (The command shodan count wordpress 1.4.7 is used to search Shodan for the number of web servers running version 1.4.7 of WordPress. This can be useful in a bug bounty program to identify potential targets that might be running a vulnerable version of WordPress.)

- shodan download wordpressfile “wordpress 1.4.7” (Downloads a json.gz file) (The command shodan download wordpressfile "wordpress 1.4.7" is used to search Shodan for files related to WordPress version 1.4.7 and download them. This can be useful in a bug bounty program to analyze the specific version for potential vulnerabilities.)

### Gunzip:

- Gunzip File.jason.gz (unzip .gz file)

### Gedit:

- sudo apt install gedit (Install Gedit)

- gedit File.jason.gz (Edit file)

### Beautify:

https://codebeautify.org/jsonviewer

- Beautify JSON is a very useful tool for formatting and beautifying JSON data. Here are some of its main applications:

1. Formatting JSON: Converts JSON data into a more readable and organized format, adding spaces and line breaks to improve readability.

2. Validating JSON: Checks if the JSON data is valid and corrects errors if necessary.

3. Visualizing JSON: Displays JSON data in a hierarchical view, making it easier to navigate and understand the structure of the data.

4. Debugging: Makes it easier to identify and fix errors in your JSON data.

5. Compatibility: Facilitates working with APIs that use JSON, making the data easier to read and handle.

- These functions are especially useful for developers and people who work with APIs, as they help to analyze, debug, and better understand JSON data.

- (Copy the info in the file.jsonwith gedit and paste it in the Beautify JSON web tool, then press Beautify to properly read the content.)

- host yahoo.com (gives us a range of IP addresses that are running on yahoo.com)

- ping yahoo.com (gives us the IP addresses that we are able to ping)

### Burp suit:

Open burp suit/proxy/intercept
open website look for www.yahoo.com
and we ccan see in the request the IP reached for the especific domain.

- shodan host IP (It will give us this information): City, Country, Organization, Updated, Number of open ports, Ports information, Ports, SSL Versions.

- shodan scan submit IP (To Scan a network)

# Hurricane Electric

- El sitio web BGP.he.net es una herramienta creada por Hurricane Electric que se utiliza principalmente para 
  obtener información relacionada con el sistema de enrutamiento global de Internet basado en el protocolo BGP 
  (Border Gateway Protocol). Este sitio es ampliamente utilizado por administradores de redes, investigadores y 
  profesionales de seguridad informática para realizar análisis de redes. Sus principales funciones son:

1. Información sobre ASN (Autonomous System Numbers):
   Muestra detalles de sistemas autónomos (AS), como sus prefijos anunciados, peers (conexiones BGP con otros AS), 
   rutas y el historial de cambios en la red.
2. Exploración de Prefijos IP:
   Permite buscar rangos de direcciones IP y ver qué AS los administra, junto con la información asociada.
3. Estado de Peering:
   Ofrece estadísticas sobre conexiones BGP entre diferentes AS, incluyendo detalles de quién está anunciando rutas 
   y hacia dónde.
4. Monitoreo de Rutas BGP:
   Ayuda a rastrear cómo se propagan las rutas en Internet y a detectar problemas como rutas inalcanzables o mal 
   configuradas.
5. Información Histórica:
   Proporciona un historial de cambios en los prefijos IP y en las configuraciones de enrutamiento, útil para 
   auditorías o investigaciones de problemas de conectividad.
6. Estadísticas Globales:
   Contiene gráficos y tablas con datos sobre la cantidad de prefijos anunciados globalmente, el crecimiento de los 
   ASN y otras métricas relevantes del ecosistema de Internet.
7. Verificación de Peering en el "Hurricane Electric IPv6 Peering Portal":
   Si tienes una cuenta, puedes usar el sitio para administrar o verificar conexiones de peering con Hurricane 
   Electric.

- Ejemplo de Uso:
  Si introduces un número de AS (como el AS15169 de Google), obtendrás información completa sobre los prefijos IP 
  que gestiona, sus peers y las rutas anunciadas.

- Aplicaciones:
  Diagnóstico de problemas de red: Como interrupciones o malas configuraciones de rutas.
  Planificación de peering: Identificar socios potenciales para conexiones BGP.
  Seguridad y análisis forense: Investigar anomalías en el enrutamiento, como ataques BGP hijacking.
  Estudios de infraestructura: Investigar la topología de Internet a nivel global.

https://bgp.he.net/

# Shodan Dashboard:

- org Yahoo (To find the organization Yahoo)
- IP Address (will pull down all this information): Geneal information, Web technologies, Open ports
- product:Apache (To see which company use that product and check versions and if they have vulnerabilities)

- You have lots of examples in Dashboard/Search query Examples.






