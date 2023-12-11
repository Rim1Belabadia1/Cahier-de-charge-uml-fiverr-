
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
## Diagramme de séquence : 

En utilisant les méthodes du diagramme de classe, nous avons développé une structure détaillée pour notre système. Ce processus nous a permis de bénéficier d'une vision approfondie des relations entre les différentes classes et entités impliquées dans notre application. Nous avons identifié les acteurs clés et élaboré trois diagrammes de séquence distincts, mettant en lumière les interactions spécifiques pour les fonctionnalités de connexion, d'administration et d'utilisateur.

Le diagramme de classe nous a offert une base solide pour comprendre la structure statique de notre système, en décrivant les classes, leurs attributs et les relations entre elles. En utilisant ces informations, nous avons pu concevoir de manière exhaustive les diagrammes de séquence correspondants.

**Pour le diagramme de séquence "Login"**, nous avons décomposé le processus de connexion en étapes détaillées, mettant en évidence les interactions entre l'utilisateur et le système à chaque étape. Cela inclut la vérification des identifiants, la gestion des erreurs éventuelles, et les actions associées au succès de la connexion.

**En ce qui concerne le diagramme de séquence "Admin"**, nous avons examiné de près les interactions spécifiques à un administrateur, décrivant les opérations d'administration telles que la gestion des utilisateurs, la modification des paramètres système, et la prise de décision associée.

**Enfin, pour le diagramme de séquence "User"**, nous avons analysé les interactions liées aux fonctionnalités principales pour un utilisateur standard, telles que la navigation dans l'interface, la soumission de données, et la réception de résultats ou de confirmations.

La séparation des acteurs dans ces diagrammes de séquence nous a permis d'obtenir une vue claire et détaillée de l'ensemble des tâches impliquées dans chaque scénario. Cela facilite non seulement la compréhension des flux de travail spécifiques à chaque acteur, mais aussi l'identification des points de convergence et d'interaction entre les différents acteurs du système. En fin de compte, cette approche méthodique renforce la qualité de la conception de notre système et facilite le développement futur.

# Diagramme de cas d'utilisation : 
En alignement avec la méthodologie utilisée pour le diagramme de classe, nous avons étendu cette approche à notre diagramme de cas d'utilisation, garantissant une représentation détaillée et complète des fonctionnalités de notre système. Nous avons segmenté les tâches spécifiques entre les acteurs principaux, aboutissant à la création de deux diagrammes de cas d'utilisation distincts, l'un dédié à l'administrateur (Admin) et l'autre axé sur l'utilisateur standard (User).

Pour le diagramme de cas d'utilisation "Admin", chaque cas a été minutieusement décomposé pour refléter les actions et les interactions spécifiques à l'administrateur. Cela inclut la gestion des utilisateurs, la configuration du système, la surveillance des activités et toute autre fonctionnalité liée à son rôle d'administration. Chaque cas d'utilisation a été détaillé pour comprendre les scénarios associés, les préconditions et les postconditions.

Parallèlement, le diagramme de cas d'utilisation "User" a été élaboré en mettant l'accent sur les tâches et les interactions essentielles pour l'utilisateur standard. Cela comprend la navigation dans l'interface, l'accès aux fonctionnalités principales de l'application, la soumission de données, et la gestion des paramètres individuels. Chaque cas d'utilisation a été détaillé pour assurer une compréhension approfondie des actions spécifiques que l'utilisateur peut entreprendre.

La séparation des tâches entre les acteurs dans ces diagrammes de cas d'utilisation offre une clarté accrue sur les responsabilités distinctes de l'administrateur et de l'utilisateur standard. Cela permet également une identification précise des points de convergence où les actions des deux acteurs peuvent interagir.

Cette approche méthodique renforce la modélisation de notre système, facilitant la communication des exigences fonctionnelles entre les membres de l'équipe de développement et assurant une base solide pour la phase de mise en œuvre. Les diagrammes de cas d'utilisation constituent ainsi un outil puissant pour guider le processus de développement en mettant en évidence les fonctionnalités clés et les interactions au sein de notre système.







   Trello : https://trello.com/b/RLtIEuLr/mod%C3%A8le-kanban-for-uml


 


 
Figure : 
- **UseCase** : Admin.moo / DCUMLD_1.moo
- **DDS** : 
- Login : ModeleOrienteObjet1.moo
- User : ModeleOrienteObjet2.moo
- Admin :ADINDSQ.moo
- **DDC** : projetuml.moo



