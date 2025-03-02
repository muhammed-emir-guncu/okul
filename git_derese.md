# git

## git temelleri

'git status'

klasörde git reposu var mı yok mu ona bakar
varsa durumu hakkında  bilgi verir

'git init'

git repo'su oluşturur

'git config --global user.name "emirgnc"'

kullanıcı ismi tanımlar
--global tanımlanan kimliği globalde kullanır

'git config --global user.email "deneme.mail.com"'

mail tanımlar.

'git config --global --get user.email'

'git config --global --get user.name'

kullanıcı ismini ve mailini verir

### çalışma alanı, index, local repo

çalışma alanı : projemizin ana klasörüdür


index : geçici alandır değişiklikri git'e atmdan önce burda tutulur.


local repo : index'teki dosyaların atıldığı ve git'in takip ettiği değişiklikler burdadır.
işlem tamam olduğunda yani eklenecek özellik hazır olduğunda commit edilmeli

'git add dosya_adı.txt'

dosyayı index'e atar

'git add .' 

bu şeklide bütün dosyaları index'e atarsın hepsiyle tektek uğraşmazsın.

'git commit'

dosyayı local repoya atar. eğer bu şekilde kullanırsan editörde sana bir yorum dosyası oluşturur
zira commitlerde yorum atman gerekir. bu yorumlar kısa ve öz olmalı.

'git commit -m "yorum"'

yorumu kendin terminalde yazarsın

'git log'

yapılan değişiklikleri commitleri gösterir

'.gitignore' dosyası oluşturup içine yok sayılacak dosyaların ismini yazarsak onu takip etmez.
github gitignore aratıp uygun dosyaları bulabilirisn.

## branch ve merge

head senin hangi konumda olduğunu gösterir

'git branch'

konumunu gösterir

'git branch dalın_adı'

branch oluşturulur

'git switch dalın_adı'

o branch'e geçiş yapar

'git merge dalın_adı'

bulunduğunuz branch ile dalın_adı isimli branch'i bulunduğunuz dalda birleştirir.

'git restore'

değişiklileri iptal eder 

'git stash'

değişiklikleri geçici bir alana kaydeder ve değişiklikleri iptal eder.

'git stash pop'

kaydedilen stash'e gider

'git stash list'

stashler listelenir

'git stash apply stash_adı'

stash_adı isimli stash'e gider

'git stash clear'

stash listesini siler

'git restore'

en son alınmış commite gider

'git restore dosya_adı'

dosya_adı isimli dosyayı eski haline getiri

'git checkout commit_hash_değeri'

commit_hash_değeri hashli commit'e geri gider.
bu gidilen commit'in branch'i yoktur yani başıboştur.
burdan yeni branch açıp devam etmek bir yöntemdir.

eski commitler hala durur.

'git reset commit_hash_değeri'

commit_hash_değeri hashli commite gider onu head yapar. 

'git reset --hard commit_hash_değeri'

commit_hash_değeri hashli commite gider. aradakileri değişiklikleriyle birlikte siler.

'git revert commit_hash_değeri'

commit_hash_değeri hashli commite gider diğer commitler durur işlemler.
o commitden devam eder.

'git diff'

durumlar arasındaki farkları gösterir