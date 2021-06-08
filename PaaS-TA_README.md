## 01. Check the commit contents
> [enable cce](https://github.com/PaaS-TA/routing-release/commit/4009a819c17cf308440a79c3de81bc651eec4518)

## 02. Submodule modify : lib/pq (src/github.com/lib/pq)
> pull v1.10.0 lib/pq
``` 
$ rm -rf src/github.com/lib/pq
$ mkdir -p src/github.com/lib/pq
$ git clone https://github.com/lib/pq.git -b v1.10.0 src/github.com/lib/pq
```

## 03. Submodule modify : go-sql-driver/mysql (src/github.com/go-sql-driver/mysql)
> pull v1.4.1 go-sql-driver/mysql
``` 
$ rm -rf src/github.com/go-sql-driver/mysql
$ mkdir -p src/github.com/go-sql-driver/mysql
$ git clone https://github.com/go-sql-driver/mysql.git -b v1.4.1 src/github.com/go-sql-driver/mysql
```

## 04. Submodule modify : jinzhu/gorm (src/github.com/jinzhu/gorm)
> pull 466b344ff5924029ad8426073ba5064093e18a22 jinzhu/gorm
``` 
$ rm -rf src/github.com/jinzhu/gorm
$ mkdir -p src/github.com/jinzhu/gorm
$ git clone https://github.com/jinzhu/gorm.git src/github.com/jinzhu/gorm
$ cd src/github.com/jinzhu/gorm
$ git checkout 466b344ff5924029ad8426073ba5064093e18a22 

```
