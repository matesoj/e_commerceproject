Projekt E-commerce Data-set
WORKFLOW
1. 	Import danych z kaggle - https://www.kaggle.com/datasets/prachi13/customer-analytics?resource=download (FORMAT .csv)
2. 	Dodanie tła w formacie .svg 
3. 	Załadowanie danych do PowerBI + transformacje w PowerQuery:
- dodanie kolumny (Date_of_order), dzięki której każde zamówienie uzyska losową datę pomiędzy (01.01.2024, a 31.07.2024)  
- dodanie kolumny (Month_of_order) (na podstawie kolumny z datą (Date_of_order) - Użycie Data.Month(Data.From([Date_of_order])).
- zmiana typu danych
4. 	Dodanie miary DAX (Orders_in_month) z użyciem CALULATE() oraz ALLEXCEPT() w celu wyłączenia filtrowania z wyjątkiem (Month_of_order)
5.	Dodanie i formatowanie fragmentatora z wartością (Month_of_order)
6.	Dodanie i formatowanie wizualizacji (Tabela) z "Dzień" z wartości (Date_of_order) oraz Liczba[ID] - wizualizacja przedstawia liczbę zamówień z podziałem na dzień miesiąca
7.	Dodanie i formatowanie wizualizacji (Skumulowany wykres kolumnowy) z wartości Liczba[ID] - oś Y, oraz Warehouse_block - oś X - przedstawienie liczby zamówień z podziałem na magazyny - celem jest dynamiczny ranking magazynów za dany okres
8.	Dodanie miary DAX (All_orders) z użyciem CALULATE(), COUNT(), DIVIDE() w celu wyliczenia procentowego udziału wartości (Orders_in_month) we wszystkich dostępnych zamówieniach
9.	Dodanie i formatowanie wizualizacji (Tabela) z wartościami (Customer_rating) oraz (ID) - przedstawienie rozkładu kategorii klientów, a liczby zamówień
10. 	Dodanie miary DAX (OnTime_orders) z użyciem CALCULATE(), DIVIDE() w celu wyliczenia procentowego udziału zamówień zrealizowanych terminowo)
11.	Dodanie i formatiowanie wizualizacji (wykres liniowy) w celu prezentacji liczby zamówień w zależności od dnia miesiąca
12.	Dodanie miar DAX (OnTime_1) oraz (OnTime_0) w celu uzyskania liczby zamówień (nie)zrealizowanych na czas
13.	Dodanie wizualizacji typu wykres kołowy przy użyciu miary (OnTime_1) oraz (OnTime_0)
14. 	Dodanie i formatowanie fragmentatorów na podstawie (Mode_of_shipment) 
15.	Weryfikacja funkcjonowania dashboardu
16. 	Eksport projektu