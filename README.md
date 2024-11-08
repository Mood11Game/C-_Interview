    Умные указатели в С++

Сами по себе указатели являются очень мощным, но в тоже время опасным инструменом, достаточно немного отвлечься и вся программа ломается. За каждым new должен идти delete иначе утечки памяти не избежны. Более того выделение динамической памяти под массивы необходимо удалять с помощью оператора delete[].

    В чем заключается суть умных указателей

  Фактически умные указатели обеспечивают автоматическое управление памятью, когда указатель выходит из области видимости запускается деструктор и память очищается. Умные указатели это классы, в которые оборачиваются обычные указатели.

    Типы умных указателей 

В 11 стандарте появилось 3 умных указателя:
  
unique_ptr-
    
shared_ptr-умный указатель, владеющий разделяемым динамически     выделенным ресурсом. Несколько таких указателей могут владеть одним и тем же ресуром, счетчик внутренний, очистка идет только после удаления самого первого указателя
    
weak_ptr- подобен shared_ptr, но не увеличивает счетчик
  
auto_ptr-не успользуется(устаревший)
    
