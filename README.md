
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

Bookmark:
Attributs:
BMID: int
user: User
gig: Gig_Service
bookmarkeddate: Date
Méthodes:
addbm(): void
remove(): void
viewBMGigs(): void

Analytics:
Attributs:
AnalyticsID: int
user: User
data: String
timestamp: DateTime
Méthodes:
collectdata(): void
analyzdata(): void
generatereport(): void

LegalDocument:
Attributs:
documentid: int
type: String
content: String
user: User
Méthodes:
uploaddoc(): void
viewdoc(): void

Subscription:
Attributs:
subid: int
user: User
startdate: Date
enddate: Date
Méthodes:
subscribe(): void
removesub(): void
viewubgigs(): void

Advertisement:
Attributs:
adID: int
content: String
enddate: Date
targetaudiance: User
startdate: Date
Méthodes:
createad(): void
updatead(): void
analyzAdPreformance(): void

Event:
Attributs:
eventid: int
name: String
descrp: String
date: Date
location: String
participants: User
Méthodes:
creationevent(): void
updateevent(): void
cancelevent(): void

Badge:
Attributs:
badgeID: int
name: String
description: String
users: User
Méthodes:
awardbadge(): void
updatebadgedetails(): void
User
Attributs :

UserID: int
Username: string
Email: string
Password: string
Méthodes :

login(email: string, password: string): void
logout(): void
Message
Attributs :

MessageID: int
Content: string
Sender: User
Timestamp: java.util.Date
Méthodes :

sendMessage(): void
Gig (Service)
Attributs :

GigID: int
Title: string
Description: string
Price: float
Seller: User
Méthodes :

create(): int
edit(): void
delete(): void
Chat
Attributs :

ChatID: int
Participants: List<User>
Messages: List<Message>
Méthodes :

addParticipant(): void
sendMessage(): void
Skill
Attributs :

SkillID: int
Name: string
Description: string
Gigs: List<Gig>
Méthodes :

addSkill(): void
updateSkillDetails(): void
Promotion
Attributs :

PromotionID: int
DiscountPercentage: float
StartDate: Date
EndDate: Date
ApplicableGigs: List<Gig>
Méthodes :

applyPromo(): void
updatePromo(): void
expirePromo(): void
Category
Attributs :

CategoryID: int
Name: string
Méthodes :

addCategory(): void
editCategory(): void
deleteCategory(): void

   Trello : https://trello.com/b/RLtIEuLr/mod%C3%A8le-kanban-for-uml


 

 **Pour le diagramme de séquence : On a élaboré
 
Figure : 
- **UseCase** : Admin.moo / DCUMLD_1.moo
- **DDS** : 
- Login : ModeleOrienteObjet1.moo
- User : ModeleOrienteObjet2.moo
- Admin :ADINDSQ.moo
- **DDC** : projetuml.moo



