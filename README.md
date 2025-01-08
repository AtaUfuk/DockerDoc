# Docker Dokümantasyonu

<b>docker ps</b>=> çalışan containerları gösterir  
<b>docker ps -a</b> => var olan tüm containerları gösterir  
<b>docker images</b> => indirilen imageları gösterir  
<b>docker run -name "container özel ismi"/"kurulmak istenen container gerçek ismi"</b> => istenilen container'ı yoksa indirip kurarak çalıştırır.  
<b>--->docker run -it -e POSTGRES_PASSWORD=1234</b> postgres ekstra parametre tanımlanarak containerın çalıştırılarak bu containera ait terminal oluşturulmasını sağlar  
<b>docker-compose up -d</b> => arkaplan görevi olarak containeri/containerları çalıştırır(-d parametresinden dolayı)  
<b>docker exec -it "container ismi veya container id si" /bin/sh</b> => çalışan containera dışarıdan komut çalıştırma/terminal oluşturma  
<b>docker search container_adı</b> => internet üzerinden istenilen bir containerı arayarak verilen derecelendirmeye göre yukarıdan aşağı sıralama yapar  
<b>docker start container_adi</b> => belirtilen container adına göre durdurulmuş olan bir işlemi tekrardan başlatır  
<b>docker update --restart unless-stopped container_adi</b> => Belirtilen container'ın docker tekrardan çalıştırıldığında otomatik olarak ayağa kalkmasını sağlar.  
<b>docker pull container_adi:versiyon(optional)</b> =>container'ı local'e indirmeyi sağlar  
<b>docker rmi image-id </b>docker da istenilen bir image'ı kaldırmak için kullanılır  
<b>docker rmi image-id image-id ... </b>=> docker daki istenilen imageları kaldırmak için kullanılır  
<b>docker rmi $(docker images -q)</b> => docker daki tüm imageları kaldırmak için kullanılır  
<span><b>docker run --name redis-test -p 5002:6379 -d redis</b><span>  
<b>docker run -p 6379:6379 -d redis --name [your_container_name] --restart unless-stoped</b> =>6379 portunda[-p] belirtilen isme göre[--name] yeni bir container oluşturur[run](İlgili image yoksa da indirip kurar) ve docker tekrardan başlatıldığında otomatik olarak ayağa kalkmasını sağlar.[--restart unless-stoped]  
<b style="color:blue;">docker inspect ContainerID/image </b> => Sonuna yazılan container id'si/image adına ait json formatta ayrıntılı bir bilgi dökümü sağlar.(Örneğin:docker inspect rabbitmq:3.12-management)  
<b style="color:blue">Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform</b> => Power Shell komutudur ve bu komut ile sanal makinenin tekrardan çalıştırılması sağlanır.
