### Découpage de réseau IP
 
 1.  **Méthode symétrique:** 

- C'est Pôle Informatique a besoin plus de adresses : 50 équipements donc necessite 52 addresses IP.
  Les sous-réseau sont la taille /26 (64 adresses).

- voici le decoupage pour les 4 sous-réseaux:
  
|   | **Adresse réseau** | **Adresse de broadcast** | **Adresse de début de plage** | **Adresse de finde plage**|
|--------------------------|--------------------------|-------------------------------|------------------------|------------------------|
| Pôle Informatique       | 172.16.1.0/26   | 172.16.1.63  |172.16.1.1 |172.16.1.62 |
| Pôle Développement      | 172.16.1.64/26 | 17.16.1.127  |172.16.1.65 |172.16.1.126 |
| Pôle Administratif     | 172.16.1.128/26 | 172.16.1.191 |172.16.1.129 |172.16.1.190|
| Pôle Techncien         | 172.16.1.192/26|172.16.1.255|172.16.1.193 | 172.16.1..254|

2.  **Méthode Asymétrique:**
- Les calcules pour chaque pôle selon leur besoin:
   . Pôle Informatique (50): 2^6-2 =62
   . Pôle Développement (12): 2^4-2 =14
   . Pôle Administratif (20): 2^5-2 =30
   . Pôle Technicien (15): 2^5-2 =30
  
- voici le découpage pour les 4 sous-réseaux:
  
|   | **Adresse réseau** | **Adresse de broadcast** | **Adresse de début de plage** | **Adresse de finde plage**|
|--------------------------|--------------------------|-------------------------------|------------------------|------------------------|
| Pôle Informatique       |172.16.1.0/26 |172.16.1.63 | 172.16.1.1| 172.16.1.62|
| Pôle Administratif      | 172.16.1.64/27 |172.16.1.95| 172.16.1.65|172.16.1.94 |
| Pôle Technicien     |172.16.1.96/27| 172.16.1.128 | 172.16.1.97|172.16.1.127|
| Pôle Développement|172.16.1.128/28|172.16.1.143|172.16.1.129 |172.16.1.142 |

