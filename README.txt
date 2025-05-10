Установка Microsoft Office 
office deployment tool по сути не нужен, так как он скачивает setup.exe и базовую конфигурацию как в папке office

Вот ссылка на видео, по которому составлен гайд
https://www.youtube.com/watch?v=TA3z0SBkdVQ&list=PLYVe-k_ciabymNZu4CKvHD2v5EdyCNhX5&index=6

1. В папке office редактируем конфиг, если нужно. Там указано скачать офис 2021 года (PowerPoint, Excel, Word)
Вот документация по параметрам конфигурации: 
https://learn.microsoft.com/ru-ru/microsoft-365-apps/deploy/office-deployment-tool-configuration-options

2. Открываем командную строку от имени администратора и пишем 
reg add "HKCU\Software\Microsoft\Office\16.0\Common\ExperimentConfigs\Ecs" /v "CountryCode" /t REG_SZ /d "std::wstring|UA" /f

3. Выполняем 
setup.exe /configure configuration-Office2021Enterprise.xml 
