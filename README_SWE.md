Guide till alternativ lösning för notifikationer via Nodered (27/10/25)
Det finns en funktion i IoT Open som heter metric_monitor, den kan ställas in på tid och rapporterar om en installation, enhet, eller funktion inte hört av sig på inställd tid. Den här nodered flowen gör att det även kan skickas ett automatiskt meddelande när detta inträffar.
1.
Öppna den medföljande filen metric_notify_tempfix.jsonKopiera innehållet (CTRL + A, CTRL + C)
2.
Starta Nodered.
Öppna menyn och välj import. Välj ”import to” (längst ner): new flow om du vill ha den här flow:en separat. Klicka in dig i fönstret och använd CTRL – V för att kopiera in koden.
3.
Dubbelklicka på den första noden ”lynx in”. Tryck på ”+” för att lägga till en server.
4.
Fyll i de tre första raderna name/url/broker. (här gäller det att ha koll på de olika uppgifterna)
5.
Sista fältet API nyckel hämtas hos iotopen.se – huvudsida / användare / välj din egen användare / säkerhet / API Nycklar / API Nycklar + / Skriv in ett namn / Skapa API nyckel / Koperia nyckeln till raden API-key i nodered.
6.
Tryck på ”Update” (röd knapp), därefter på ”Done”.
7.
Dubbelklicka på noden ”Lynx get-meta” och se till att ”function” har samma namn som i första noden (om ”settings from flow” är ifylld klicka ur den och se till att ”function” har samma namn som i första noden)
8.
Dubbelklicka på noden ”lynx notification”. Ställ in server/installation/output och klicka på ”output configuration” så att fönstret öppnas.
9.
Fyll i fältet Name med valfritt namn/ Välj Executor: välj mellan olika lösningar, default är IoT Open Mail. vissa installationer har SMS och push notiser också.
10.
Message: genom att klicka på ”+” på raden ”Message” kan man skapa ett helt nytt meddelande att skicka ut, alternativt kan man klicka på pennan för att ändra det befintliga.
11.
recipients (detta behövs, glöm inte s:et på slutet) *Om fler mottagare ska fyllas i så skriver man ett kommatecken i mellan, t.ex.gustav.hedenborg@gmail.com, nodered@gmail.comm
subject (alternativt) *För SMS behövs inte subject
12.
Glöm inte att trycka på den röda knappen deploy. Uppe till höger.

[guide_notifications_nodered.pdf](https://github.com/user-attachments/files/18575592/guide_notifications_nodered.pdf)
