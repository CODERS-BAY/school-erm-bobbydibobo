# Library NF

Book(BookID,ShelfID,pubHouse,intCopies,sinceBrw,transTemp,reserved)
Journal(journalID,shelfID, pubHouse)
Article(keyword, relevance, references)
Costumer(PD, brwBooks, returns, reservations)
Employee(ID, brwManage)
Shelf(ID,stock,freeSlots)
SubArea(ID, book, journal, article)


## Assos

Book-1---n-Book_contains_Article-1---n-Article
key1:BookID
key2:keyword

Journal-1---n-Journal_contains_Article-1---n-Article
key1:JournalID
key2:keyword

Shelf-1---n-Shelf_stores_Book-n---1-Book
key1:ShelfID
key2:BookID

Shelf-1---n-Shelf_stores_Journal-n---1-Journal
key1:ShelfID
key2:JournalID

Costumer-1---n-Costumer_borrows_Book-n---1-Book
key1:CostumerSVN
key2:BookID

Costumer-1---n-Costumer_reads_Journal-n---1-Journal
key1:CostumerSVN
key2:JournalID

Employee-1---n-Employee_protecc_Journal-n---1-Journal
key1:EmployeeID
key2:JournalID

