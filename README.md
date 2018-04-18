# Úloha k workshopu

Na stránce https://www.elastic.co/products si stáhněte a zprovozněte Elasticsearch, Kibanu a FileBeat.

### Spuštění na Windows:
Pro spuštění Elasticsearch zadejte do příkazového řádku příkaz bin\elasticsearch.bat.
Pro spuštění Kibany musíte mít zároveň spuštěný Elasticsearch. Chcete-li změnit defaultní konfiguraci Kibany, otevřete soubor config\kibana.yml a soubor upravte.  Poté použijte příkaz bin\kibana.bat.
Před spuštěním Filebeatu upravte konfigurační soubor filebeat.yml. Poté spusťte Filebeat příkazem filebeat.exe. 
Zda vám vše běží můžete průběžně kontrolovat přes prohlížeč (localhost:9200 pro Elastisticsearch, localhost:5601 pro Kibanu).

### První úkol:
Nahrajte všechny soubory ze složky log do elasticsearche za použití filebeatu.
Jakmile začne Filebeat zpracovávat data, tak se v Kibaně objeví nově vytvořený index.
Vytvořte si pro to index-pattern, který bude pracovat s indexy. Výsledný pattern bude vypadat takto "filebeat-*".
V dalším kroku si nastavte @timestamp jako Time Filter field name, aby se vám data dala správně filtrovat podle času.
Jakmile vše nastavíte, tak se přepněte na záložku Discover, kde uvidíte časovou osu a záznamy, které přibývají.

### Druhý úkol:
Upravte FileBeat, abyste měli vaše logy otagované (projekt, error, info, debug).
