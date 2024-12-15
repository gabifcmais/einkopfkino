function generator(){

            var wordlist1 = ["Cool","Masked","Tricky","Lovely","Big","Einstein","White","Rotten",
                            "Blue","Black","Fancy","Red","Purple","Golden","Silver", "Queen", "King", "Gentle", "Tiny", "Teeny", "Silly", "Naughty", "Dear", "Sugar", "Sweet",
                            "Agile", "Amazing", "Awesome", "Dainty", "Bright", "Noisy", "Nosy", "Quick", "Quiet", "Sassy", "Saucy", "Sharp", "Timid", "Touchy", "Snazzy", "Pretty", "Lazy",
                            "Spirited", "Flaky", "Flashy", "Elfin", "Fiery", "Ferocious", "Bubbly", "Fussy", "Fiery", "Funny", "Gentle", "Gloomy", "Good", "Grouchy", "Crabby", "Cool", "Cranky", "Curious", "Hearty", "Hot-headed", "Electric", "Master"  ];

            var wordlist2 = ["Cavy","Moose","Llama","Duck","Bear","Eagle","Tiger",
                            "Rocket","Bullet","Knee","Foot","Hand", "Yuki", "Aspen", "Tut", "Apollo", "Bandit", "Smokey", "Misha", "Snow", "Snowball", "Lord", "Prince", "Princess",
                            "Giant", "Dwarf", "Sally", "Bee", "Star", "Dragon", "Buddy", "Lady", "Urchin", "Champion", "Cherub", "Oreo", "Soul", "Guy", "Emir", "Earl", "Admiral",
                            "Baron", "Baroness", "Bishop", "General", "Chief", "Emperor", "Majesty", "Master", "Boss", "Captain", "Duchess", "Skipper", "Czar", "Tyrant", "Raja", "Dame",
                            "Colonel", "Khan", "Knight", "Duke", "Jewel", "Mate"  ];

            // Random numbers are made 
            var randomNumber1 = parseInt(Math.random() * wordlist1.length);
            var randomNumber2 = parseInt(Math.random() * wordlist2.length);
            var name = wordlist1[randomNumber1] + " " + wordlist2[randomNumber2];           

            //alert(name); //Remove first to slashes to alert the name

            //If there's already a name it is removed  
            if(document.getElementById("result")){
                document.getElementById("placeholder").removeChild(document.getElementById("result"));
            }
            // A div element is created to show the generated name. The Name is added as a textnode. Textnode is added to the placeholder.
            var element = document.createElement("div");
            element.setAttribute("id", "result");
            element.appendChild(document.createTextNode(name));
            document.getElementById("placeholder").appendChild(element);
        }       
