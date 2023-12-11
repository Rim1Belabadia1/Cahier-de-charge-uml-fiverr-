
[Update - 29/10-2023 ]


### Diagramme de Classe


Introduction:
Ce diagramme de classe représente le systéme Fiverr :

Classes et structures:

Order:

Attributs:
OrderId: int
gig: Gig_Service
Status: String
Buyer: User
Méthodes:
PlacerOrder(): void
CancerOrder(): void
UpdateStatus(): void
PFITEM:

Attributs:
itemID: int
title: String
description: String
imageURL: String
PF: Portofilio
Méthodes:
updateitemdetailms(): void
Portofilio:

Attributs:
PID: int
user: User
Pfiftems: int
Méthodes:
addPF(): int
addPF(): void
EditPF(): void
removePF(): void
Report:

Attributs:
ReportOID: int
reason: String
ReportedUser: User
reporterbyUser: User
Méthodes:
submitreport(): void
processreport(): void
resolvereport(): void
Review:

Attributs:
reviewID: int
Order: Order
rating: int
comment: String
Méthodes:
addReview(): void
editReview(): void
Payement:

Attributs:
payID: int
amout: float
order: Order
Notification:

Attributs:
notifID: int
message: Message
user: User
Méthodes:
sendnotif(): void
markread(): void
Invoice:

Attributs:
Invoiced: int
order: Order
amount: float
Status: String
Méthodes:
GénérateInvoice(): void
upadate(): void
Contract:

Attributs:
Contract id: Int
order: Order
delevryDate: Date
Status: String
Méthodes:
CreateContracte(): void
updatestatus(): void
extenddelivrydate(): void


   Trello : https://trello.com/b/RLtIEuLr/mod%C3%A8le-kanban-for-uml


 

 
 
Figure : 
- **UseCase** : Admin.moo / DCUMLD_1.moo
- **DDS** : 
- Login : ModeleOrienteObjet1.moo
- User : ModeleOrienteObjet2.moo
- Admin :ADINDSQ.moo
- **DDC** : projetuml.moo



