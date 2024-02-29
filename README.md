eng below

API_OPERATIONS.PY
	Kod wysyłający zapytania do API oraz przetwarzający otrzymane dane, zbudowany w oparciu o podział na funkcje dostarczające konkretnych informacji
./ORACLE_SQL
	Folder z procedurami/triggerami/funkcjami wykorzystywanymi w lokalnej bazie danych postawionej na Docker. Baza dzieli się na tabele RAW/FINAL co pozwala odseparować surowe dane od finalnych. Trigger raw_data_id tworzy id dla każdego nowo wgranego wiersza. Przetwarzanie danych między tabelami umożliwia procedura PROCESS_RAW_DATA budująca funkcję merge. Ewentualne błędy raportowane są w tabelach err$_table_name.
APIFOOTBALL_DAG.PY
	Kod DAG Apache Airflow wraz ze zdefiniowanymi taskami. FInalne dane są przetwarzane bazując na połączeniu zadeklarowanym w UI Airflow.
	

-----------------------------------------------------------------------------
-------------------------------- ENG ----------------------------------------
-----------------------------------------------------------------------------

API_OPERATIONS.PY
	Code that sends queries to the API and processes the received data, built on the basis of a breakdown of functions that provide specific information.
./ORACLE_SQL
	Folder with procedures/triggers/functions used in a local database put on Docker. The database is divided into RAW/FINAL tables which allows to separate raw data from final data. The raw_data_id trigger creates an id for each newly uploaded row. Processing data between tables is possible by the PROCESS_RAW_DATA which builds merge function. Any errors are reported in the err$_table_name tables.
APIFOOTBALL_DAG.PY
	Apache Airflow DAG code with defined tasks. FInal data is processed based on the Oracle connection declared in the Airflow UI.
