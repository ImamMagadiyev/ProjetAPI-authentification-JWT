# ProjetAPI

Une application web full-stack avec authentification JWT, construite en PHP/MySQL et déployée sur serveur Apache.

🔗 **[Accéder à la prod](https://r301.kilya.coop/)** — Identifiants : `admin` / `admin`

---

## 🛠️ Technologies utilisées

- **Frontend** — HTML, CSS
- **Backend** — PHP, PDO
- **Base de données** — MySQL
- **Authentification** — JWT (JSON Web Tokens)

---

## ⚙️ Installation & Configuration

### Prérequis

Modules Apache à activer :
```bash
sudo a2enmod php php-mysql rewrite
```

### Virtual Host Apache

```apache
<VirtualHost *:80>
    ServerName ${serverName}
    DocumentRoot /var/www/${serverName}

    <Directory "/var/www/${serverName}">
        Options Indexes FollowSymLinks
        AllowOverride None
        Require all granted
    </Directory>

    RewriteEngine On
    RewriteCond %{REQUEST_URI} !\.(css|jpg)$
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^ index.php [QSA,L]
</VirtualHost>
```

> Remplacer `${serverName}` par le nom de domaine ou l'IP du serveur.

---

## 📁 Structure du projet

```
ProjetAPI/
├── AuthAPI/              # Gestion de l'authentification
├── ProjetAPI-Backend/    # Logique serveur et endpoints API
├── ProjetAPI-Frontend/   # Interface utilisateur
├── jwt_utils.php         # Utilitaires JWT
├── .htaccess             # Réécriture d'URL
└── .github/workflows/    # CI/CD GitHub Actions
```

---

## 👥 Contributeurs

- [@ImamMagadiyev](https://github.com/ImamMagadiyev)
- [@Adr43n](https://github.com/Adr43n)
- [@adrien399](https://github.com/adrien399)
