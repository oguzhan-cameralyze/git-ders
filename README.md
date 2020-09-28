## Git Dersi


### Git Nedir?
> Git, 2005 yılında Linus Torvalds tarafından piyasaya sürülmüştür. Yazılım geliştirme süreçlerinde kullanılan, takım çalışmasını kolaylaştıran **sürüm kontrol sistemidir.** Tamamen ücretsizdir ve kullanımı kolaydır. Alternatif örneği olarak [Mercurial](https://www.mercurial-scm.org/about)'i verebiliriz.


### Git Kurulumu
> https://git-scm.com/downloads adresinden kolaylıkla kurulabilir.


### Git Versiyonunu Öğrenme
    $ git --version
    git version 2.24.3 (Apple Git-128)
    //çıktı bu şekilde olacaktır


### Kullanıcı Konfigürasyonu
> Değişiklikleri kimin yaptığının belli olması için ve değişikliklerin tutulabilmesi için her işlemde kullanıcı/şifre bilgisi sormaması için konfigürasyon yapmamız gerekir.

    $ git config --global user.name "oguzhan-cameralyze"
    $ git config --global user.email "oguzhan@cameralyze.com"

> Konfigürasyonu kontrol etmek için ise;

    $ git config --global user.name
    oguzhan-cameralyze

    $ git config --global user.email
    oguzhan@cameralyze.com


### Local Repository Oluşturma
> Yazılımlarımızı repository içerisinde tutarız. Repository, yazılım için depolama alanıdır. Geliştiriciler arasında **Repo** şeklinde kısaltılarak kullanılır.

    $ git init
    Initialized empty Git repository in /Users/oguzhandemiroz/Desktop/foldername/.git/

    $ git status (git status ile repomuzu kontrol edebiliriz)
    On branch master

    Initial commit

    nothing to commit (create/copy files and use "git add" to track)


### Local Repository'i Remote'a Göndermek (Bağlamak)
> Repolarımızı GitHub'a yükleyebiliriz. [GitHub](http://github.com/), Sürüm kontrol sistemi olarak git kullanan yazılım geliştirme projeleri için web tabanlı depolama servisidir. Rakipleri; [BitBucket](https://bitbucket.org/), [GitLab](https://gitlab.com/) ve [AWS CodeCommit](https://aws.amazon.com/tr/codecommit/) vb. sayabiliriz.

> Remote göndermeden önce repo içerisinde dosya bulunması gerekiyor. Dosya varmış gibi devam edelim.

    $ git add .
    $ git commit -m "First Commit"
    $ git push
    fatal: No configured push destination.
    Either specify the URL from the command-line or configure a remote repository using

        git remote add <name> <url>

    and then push using the remote name

        git push <name>
    
    // yukarıdaki gibi uyarı verecektir. Remote bağlantı yapmamız gerektiğini hatırlatıyor.

    $ git remote add reponame https://github.com/oguzhan-cameralyze/reponame.git


### Remote Repository'i Local'e Çekmek
> Repolarımızı GitHub'dan Local'e çekebiliriz.

    $ git clone https://github.com/oguzhan-cameralyze/reponame.git


### Git Add Nedir?
> Belirttiğimiz bir dosyayı ya da tüm projeyi çalışma dizinine(index) ekler. Yani commit'lenmeye hazır hale getirir.

> . (nokta) tüm dosyaları dizine ekler.
> 
> Add'den sonra dosya adını belirtirsek sadece o dosyayı ekler.

    $ git add .

    $ git add README.md


### Git RM Nedir?
> Belirttiğimiz bir dosyayı ya da tüm projeyi çalışma dizininden(index) siler.

> . (nokta) tüm dosyaları çalışma dizinden siler.
> 
> Add'den sonra dosya adını belirtirsek sadece o dosyayı çalışma dizininden siler.

    $ git rm .

    $ git rm README.md


### Git Commit Nedir?
> Commit, **işlemek** anlamına geliyor. Git eklediğimiz dosyaları kalıcı olarak GitHub'a işlemeye commit denir. -m argümanı ile işleme yaparken yaptığımız değişikliği belirtebiliriz. m: messages'ın kısaltmasıdır.

    $ git commit -m "a.txt dosyasının içeriği değiştirildi"


### Git Push Nedir?
> Repo'da yaptığımız değişikleri remote'a göndermemizi sağlayan komut.

    $ git push


### Git Pull Nedir?
> Repo'da yaptığımız değişikleri local'e çekmemizi sağlayan komut.

    $ git pull


### Branch Nedir?