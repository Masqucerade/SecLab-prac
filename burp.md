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











