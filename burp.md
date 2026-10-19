после многих предложений стоят точки из-за попытки добавления многократных пробелов после строки для автоматического переноса (enter) в формате .md


### [ ] Как отфильтровать HTTP History? Что такое scope?
Proxy -> HTTP history -> Filter. 
<img width="1016" height="346" alt="telegram-cloud-photo-size-2-5384504455396531279-y" src="https://github.com/user-attachments/assets/bbead23e-eea6-40ba-ac86-da880deef1a2" />
дальше просто выбираем что нам нужно. 
тип.запроса/MIME.type/статус.ответа/расширения/метки и тд. 
<img width="1280" height="522" alt="telegram-cloud-photo-size-2-5384504455396531280-y" src="https://github.com/user-attachments/assets/3becd4f3-3432-471e-b763-1df105233cc6" />
Далее, scope - цели, т.е список хостов которые являются нашими целями в сессии. 
Можно фильтровать только на <show only in scope>. Можно в Target->Scope, либо напрямую тыкнув правой кнопкой на адрес ссылки и Add to Scope. 
<img width="991" height="400" alt="image" src="https://github.com/user-attachments/assets/6386fd65-1303-441d-8b2f-d9dfb76c8be8" />
<img width="437" height="257" alt="image" src="https://github.com/user-attachments/assets/f60c86d9-3249-4122-9f3f-107baeb83f60" />
<img width="234" height="133" alt="image" src="https://github.com/user-attachments/assets/c833219f-e4b2-497a-82dd-a2eef0771ad2" />. 

### [ ] Как организовать зоопарк вкладок в Repeater?  
<img width="952" height="192" alt="telegram-cloud-photo-size-2-5384504455396531299-y" src="https://github.com/user-attachments/assets/3f2e7ac2-e627-4d99-b60d-5aecb7514599" />
<img width="870" height="926" alt="telegram-cloud-photo-size-2-5384504455396531297-y" src="https://github.com/user-attachments/assets/c3c57a2c-5643-4933-aac1-0216fa83e0cb" />.  

### [ ] Какие виды атак есть в Intruder?  
Всего 4 типа атак. 
Sniper - тыкает по 1 параметру на 1 место (a,_), (_,a), (b,_), (_,b).   
Battering ram - одно значение на все позиции (a,a), (b,b).   
Pitchfork - известные пары (например логин+пароль) на свои места login1:pass1, login2:pass2     
cluster bomb - все комбинации (a,a), (a,b), (b,a), (b,b).   
<img width="932" height="295" alt="image" src="https://github.com/user-attachments/assets/7f94c3d3-6391-4d10-a773-0b9df7f6536d" />
<img width="502" height="293" alt="image" src="https://github.com/user-attachments/assets/be7c784c-3fc7-4466-9431-61d2279f6bd3" />
сюда добавляются готовые или произвольные списки с датой   

### [ ] Как контролировать RPS при атаках Intruder?   
settings -> recource pool.  
Maximum concured request - сколько максимально одновременных запросов.  
Delay between request - задержка между запросами.  
<img width="512" height="925" alt="image" src="https://github.com/user-attachments/assets/8b7d89ad-4c7a-4c80-8e48-c75f6e16b579" />.  

### [ ] Как подменить ответ сервера на запрос из Intercepter? Repeater? А как автоматически подменять ответы для живого трафика?   
Intercept (вручную) 
<img width="1223" height="423" alt="image" src="https://github.com/user-attachments/assets/f403bca1-7f63-42b3-9fe3-badbbf19353d" />
<img width="862" height="582" alt="image" src="https://github.com/user-attachments/assets/db829250-a527-471d-acfa-d313e80e8bdd" />.  
Forward -> берп ловит ответ -> редактируем тело и заголовки -> Forward -> браузер получает измененное.  
в Repeater - нельзя. Правится только запрос. Он шлет запрос напрямую и отдает ответ сервера.   

Автоматически для всего трафика можно использовать Proxy -> Match and replace.   
<img width="1236" height="466" alt="image" src="https://github.com/user-attachments/assets/8765f1ce-00f6-48c2-b194-cb1074d98747" />
<img width="1051" height="324" alt="image" src="https://github.com/user-attachments/assets/f44cc0e1-430e-46f9-9a9f-e5e6e44e9c70" />
Меняем например заголовки на лету.   

### [ ] Как провести дирбастинг средствами Intruder?   
Ловит гет, отправляем в Intruder, режим снайпера и в пути добавляем изменяющийся параметр
<img width="379" height="191" alt="image" src="https://github.com/user-attachments/assets/f6b12757-a153-470b-88ba-97df35dda58e" />.  
далее загружаем список дефолт директорий которые мы можем поперебирать.  
<img width="496" height="367" alt="image" src="https://github.com/user-attachments/assets/bd05a46e-0a0e-440f-bd0b-e67babb53a44" />. 
далее старт атаки и смотрим по коду (404 нет).  

### [ ] Как провести брутфорс Basic Auth?    
httpbin.org/basic-auth/user/passwd попробуем на этом.  
После ввода в логин и пароль 1 и 1 к нам в берп прилетает это   
<img width="659" height="486" alt="image" src="https://github.com/user-attachments/assets/b18d0e58-1b67-4f00-b11d-b292da004d13" />.   
видим Authorization: Basic MTox.   отправляем в Intruder     
выделяем пейлоад
<img width="448" height="135" alt="image" src="https://github.com/user-attachments/assets/ff3c3d40-926b-427a-942d-086e895ce361" />
и далее добавляем пары и кодируем    
<img width="410" height="146" alt="image" src="https://github.com/user-attachments/assets/16f0ce25-fff1-4d33-b508-6b564ed5557e" />
<img width="592" height="403" alt="image" src="https://github.com/user-attachments/assets/76c3b5fb-6a3d-4c7a-ae8a-ade3a5e9ed83" />
<img width="608" height="372" alt="image" src="https://github.com/user-attachments/assets/7be06653-93a7-4142-af9c-da6079a1dbd6" />
<img width="509" height="389" alt="image" src="https://github.com/user-attachments/assets/1fc6d4c8-5db5-4b6d-8b15-6bbe9fe17057" />|
и получаем 200 на user:passwd
<img width="1512" height="968" alt="image" src="https://github.com/user-attachments/assets/361114d5-d2f7-4ad5-9db7-59fda74459f4" />

### [ ] Что такое Organizer?    
органайзер - просто хранилище отправленных туда нужных запросов. 
отправляется также Send to Organaizer.  
хранит запрос и ответ отдельно не зависимо от http history.   

### [ ] Представьте, что на проекте Вам нужно анализировать трафик десктопного приложения. Обычно мы в таких случаях просто указываем адрес прокси 127.0.0.1:8080, на котором слушает Burp Suite, но в этот раз подобное не получится -- приложение не имеет настройки прокси и игнорирует системные, т.е. указать прокси для него никак не получится. При это известно (например, по анализу трафика в wireshark), что приложение все запросы отправляет на https://example.com. Как пустить трафик через Burp?
  * [ ] Для простоты вместо десктопного приложения все-таки возьмем браузер, но запрещено как-либо настраивать для него прокси, также запрещено менять системные настройки прокси. В браузере посещается адрес https://example.com, и этот запрос (как и ответ на него) должен быть виден в Burp -\> Proxy -\> HTTP History.

Приложение нельзя настроить на прокси -> делаем прокси прозрачным   
перенаправляем днс чтобы example.com резолвился в нашу машину а берп слушал как сам сервер.  

1) etc/hosts: 127.0.0.1 example.com добавить запись в файл.
2) Листенер на 443 инвизибл. <img width="1464" height="391" alt="image" src="https://github.com/user-attachments/assets/ab4f4255-c429-4440-8008-ec5e65534a16" /> ADD
   <img width="620" height="142" alt="image" src="https://github.com/user-attachments/assets/23ad4e2b-5341-472c-b472-98b5714eed04" /> и далее такие настройки
   <img width="674" height="350" alt="image" src="https://github.com/user-attachments/assets/6fef39df-c33e-4d01-be49-09302581f89e" />
3) И далее разорвать петлю Network -> DNS и добавитьб example.com -> его реальный айпи <img width="1118" height="606" alt="image" src="https://github.com/user-attachments/assets/3f01cf7c-9ddb-4e81-8e73-0ca3d57cae42" />
4) CA Burp в доверенные иначе приложение отвергнет сертификат.































