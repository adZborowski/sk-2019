System operacyjny w środowisku sieciowym
=========================================

Charakterystyka systemu operacyjnego
------------------------------------

| Charakterystyka | wartość           | komentarzu |
| ------------- |:-------------:| -----:|
| nazwa      | linux | debian 9 |
| program (parametry sieci)      | niewiem |  |


Konfiguracja połączenia sieciowego
----------------------------------

| Parametr | wartość           | komentarzu |
| ------------- |:-------------:| -----:|
| Adres IP      | 10.0.2.15 | przydzielony przez DHCP ip a|
| Maska podsieci      | 255.255.255.0 | sudo apt install net-tools -> route -n  |
| Brama      | 10.0.2.2 | ip route |
| DNS 1      | 10.10.0.8 | cat /etc/resolv.conf  |
| DNS 2      | 10.10.0.4 | cat /etc/resolv.conf  |

Schemat sieci
-------------

aby załączyć obrazek 

```markdown
![alt schemat](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)![alt schemat](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)

![alt schemat](images/my-network-schema.png)
```
