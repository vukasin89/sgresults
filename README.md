# sgresults
Java code data

1. Napisati program koji prikazuje slučajan broj u opsegu x do y. Brojevi x i y se unose sa tastature.
```
        int x;
        int y;
        int randomBroj;

        System.out.println("Unesi broj x");
        x = s.nextInt();
        System.out.println("Unesi broj y");
        y = s.nextInt();
      
        randomBroj = (int) ((Math.random() * (y - x)) + x);
        System.out.println("Random broj je " + randomBroj);
```
2.Napisati Java program za uklanjanje duplikata iz niza od 5 celobrojnih vrednosti. Program treba da uzme ulazni niz brojeva od korisnika, ukloni duplikate i prikaže rezultirajući niz bez duplikata.
```
        int[] brojevi = new int[5];       
        List<Integer> bezDuplikata = new ArrayList<>();
        
        for (int i = 0; i < 5; i++) {
            System.out.println("Unesite broj");
            int broj = s.nextInt();
            brojevi[i] = broj;
        }
        
        for(int i = 0; i < 5; i++){
            int trenutniBroj = brojevi[i];
            boolean imaDuplikata = false;
            
            for(int trenutniBrojIzDuplikata : bezDuplikata)
            {
                if(trenutniBrojIzDuplikata == trenutniBroj)
                {
                    imaDuplikata = true;
                    break;
                }
            }
            
            if(imaDuplikata == false)
            {
                bezDuplikata.add(trenutniBroj);               
            }
        }
        
        String ispisBrojeva = "";
        System.out.println("Niz brojeva je");
        for (int i = 0; i < bezDuplikata.size(); i++) {
            int b = bezDuplikata.get(i);
            ispisBrojeva += b + ", ";

        }
        System.out.println(ispisBrojeva);
```
3. Napisati Java program za proveru da li je uneti broj sa tastature prost broj veći od 30 i manji od 1000. Broj je prost ako je deljiv samo sa 1 i sam sa sobom.
```
        int broj;

        System.out.println("Unesi broj izmeju ");
        broj = s.nextInt();

        if (broj < 30 || broj > 1000) {
            System.out.println("Nije adekvatan broj");
            return;
        }

        if (broj % 2 == 0) {
            System.out.println("Parni brojevi nisu prosti");
        }

        boolean jesteProst = true;
        //boolean nijeProst = false;
        for (int delilac = 3; delilac < broj; delilac += 2) {
            if (broj % delilac == 0) {
                jesteProst = false;
            }
        }

        if (jesteProst) {
            System.out.println("prost broj");
        } else {
            System.out.println("nije prost broj");
        }
```
4. Unesi niz od 5 brojeva i ispisi indekse svih onih ciji je zbir jednak poslednjem clanu niza.
```
          int[] sviBrojevi = new int[5];

          for (int i = 0; i < 5; i++) {
            System.out.println("Unesite broj");
            sviBrojevi[i] = s.nextInt();
          }

          int zbir = sviBrojevi[4];

          for (int i = 0; i < sviBrojevi.length - 1; i++) {
            int trenutniBroj = sviBrojevi[i];

            for (int j = i + 1; j < sviBrojevi.length - 1; j++) {
              int potencijalniBroj = sviBrojevi[j];
                
              if (trenutniBroj + potencijalniBroj == zbir) {
                System.out.println("Indeksi čiji je zbir: " + zbir + " su: " + i + " i " + j);
              }
            }
          }
```
5.Unesi string i svako slovo karaktera alfabeta zameni suprotnim slovom.
```
        String[] redniNizBrojeva = {"a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z"};
        String[] obrnutiNizBrojeva = {"z","y","x","w","v","u","t","s","r","q","p","o","n","m","l","k","j","i","h","g","f","e","d","c","b","a"};
        System.out.println("Unesite rec");
        String mojaRec = s.next();

        String[] mojaRecUNizu = mojaRec.toLowerCase().split("");
        
        String naopakaRec = "";

         for (String slovo : mojaRecUNizu) {
            int index =  Arrays.asList(redniNizBrojeva).indexOf(slovo);
            
            naopakaRec += obrnutiNizBrojeva[index];
         }
         
         System.out.println("Ovako ista rec deluje suprotni: " + naopakaRec);
```
6.U main() metodu osnovne klase programa od korisnika tražite da unese podatak o tome koliko će laptopova da unese, a zatim napravite niz od toliko elemenata klase Laptop.

Pomoću adekvatne petlje izvršite unos svih podatka potrebnih da se napravi objekat klase Laptop, koji zatim treba upisati na adekvatnu poziciju kreiranog niza.

Prikazati na standardnom izlazu sve unete laptopove koji imaju više od 8 GB RAM-a i čija grafička kartica ima više od jednog jezgra.
```
        int brojLaptopova;
        System.out.println("Unesite broj laptopova koje zelite da unesete");
        brojLaptopova = s.nextInt();

        Laptop[] laptopovi = new Laptop[brojLaptopova];

        String radnaFrekvencijaProcesora;
        int brojJezgara;
        int sirinaMagistrale;
        int kolicinaMemorije;
        String nazivProizvodjaca;
        String model;
        int godinaProizovdnje;
        int velicinaDiska;
        for (int i = 0; i < brojLaptopova; i++) {
            System.out.println("Unesi broj radnaFrekvencijaProcesora");
            radnaFrekvencijaProcesora = s.next();
            System.out.println("Unesi broj jezgara");
            brojJezgara = s.nextInt();
            System.out.println("Unesi sirinu magistrale");
            sirinaMagistrale = s.nextInt();
            System.out.println("Unesi kolicinu memorije");
            kolicinaMemorije = s.nextInt();
            System.out.println("Unesi naziv proizvodjaca");
            nazivProizvodjaca = s.next();
            System.out.println("Unesi model");
            model = s.next();
            System.out.println("Unesi godinu proizvodnje");
            godinaProizovdnje = s.nextInt();
            System.out.println("Unesi kolicinu memorije");
            kolicinaMemorije = s.nextInt();
            System.out.println("Unesi velicinu diska");
            velicinaDiska = s.nextInt();
            laptopovi[i] = new Laptop(nazivProizvodjaca, model, godinaProizovdnje, kolicinaMemorije,velicinaDiska, radnaFrekvencijaProcesora, brojJezgara, sirinaMagistrale, kolicinaMemorije  );

        }
            for(Laptop l:laptopovi){
            if(l.getBrojJezgara()>1 && l.getKolicinaMemorija()>8)
                System.out.println(l.toString());
        }
```
7.Unesi string i izbrisi sve duple karaktere sem prvog pojavljivanja.
```
        System.out.println("Unesi rec");
        String mojaRec = s.next();
        String[] slovoPoSlovo = mojaRec.split("");
        List<String> bezDuplikata = new ArrayList<>();

        for (int i = 0; i < slovoPoSlovo.length; i++) {
            String treuntoSlovo = slovoPoSlovo[i];

            boolean jesteDuplikat = false;

            for (String slovoBezDuplikata : bezDuplikata) {
                if (slovoBezDuplikata.equals(treuntoSlovo)) {
                    jesteDuplikat = true;
                    break;
                }
            }
            if (jesteDuplikat == false) {
                bezDuplikata.add(treuntoSlovo);
            }
        }
        String novaRec = String.join("", bezDuplikata);
        
        System.out.println("Nova rec je " + novaRec);
```
