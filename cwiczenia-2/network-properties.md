Ustawianie parametrów sieci
---------------------------

![alt text][network]

[network]: ./network.png "Logo Title Text 2"

1. na 1 z komputerów zainstaluj oprogramowanie ``http-chat`` dostępne pod adresem ``https://github.com/jkanclerz/http-chat``

Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 10.0.15.4 | polecenie ip addr add (tutaj wpisujemy adres ip) / (tutaj podajemy maskę) |
| MASKA  | /24 (255.255.255.0) | jak wyżej |
|   |  | |
| PC 2  |  | |
| IP - address  | 10.0.15.6 | polecenie ip addr add (tutaj wpisujemy adres ip) / (tutaj podajemy maskę) |
| MASKA  | /24 (255.255.255.0 )| jak wyżej |

Weryfikacja połączenia

Polecenie
```
ping "tutaj wpisujemy adres ip"
```

Efekt
```
Otrzymujemy informację zwrotną z ilością pakietów wysłanych, odebranych i straconych.
W tym przypadku podana konfiguracja zadziała.
```

Statyczna konfiguracja parametrów połączenia
Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 192.168.10.10 |polecenie ip addr add (tutaj wpisujemy adres ip) / (tutaj podajemy maskę)|
| MASKA  | 255.255.255.0 | jak wyżej po / wpisujemy 24 |
|   |  | |
| PC 2  |  | |
| IP - address  | 172.16.100.100 | polecenie ip addr add (tutaj wpisujemy adres ip) / (tutaj podajemy maskę)|
| MASKA  | 255.255.0.0 | jak wyżej po / wpisujemy 24 |

Weryfikacja połączenia

Polecenie
```
z PC1 polecenie ping 172.16.100.100
z PC2 polecenie ping 192.168.10.10
```

Efekt
```
Otrzymujemy informację zwrotną z ilością pakietów wysłanych, odebranych i straconych.
W tym przypadku podana konfiguracja nie zadziała.
```

Nowa statyczna konfiguracja 

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 192.168.10.10 |polecenie ip addr add (tutaj wpisujemy adres ip) / (tutaj podajemy maskę)|
| MASKA  | 255.255.255.0 | jak wyżej po / wpisujemy 24 |
|   |  | |
| PC 2  |  | |
| IP - address  | 192.168.10.11 | polecenie ip addr add (tutaj wpisujemy adres ip) / (tutaj podajemy maskę)|
| MASKA  | 255.255.0.0 | jak wyżej po / wpisujemy 24 |

Weryfikacja połączenia

Polecenie
```
z PC1 polecenie ping 192.168.10.11
z PC2 polecenie ping 192.168.10.10
```

Efekt
```
Otrzymujemy informację zwrotną z ilością pakietów wysłanych, odebranych i straconych.
W tym przypadku podana konfiguracja zadziała.
```

Warto wiedzieć
--------------

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
| Lokalizacja pliku z konfiguracją sieci|  /etc/network/interfaces | |
| UP -> Wyłączenie interfejsu sieciowego| ip link set dev (nazwa urządzenia np. enp0s3) up | |
| DOWN -> Włączenie interfejsu sieciowego| ip link set dev (nazwa urządzenia np. enp0s3) down | |
| Sprawdzenie obecnych parametrów | ip addr lub ip a | |
| lista wszystkich interfejsów | ip link show | |
| Które interfejsy jakie porty słuchają | | |
