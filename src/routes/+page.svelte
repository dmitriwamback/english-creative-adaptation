<script>
    import katex from "katex";
    import "katex/dist/katex.min.css";

    const prologueMessages = ['April 20 1980, Qair invades Prankutostan. Qairi puppet governments in Snzaq, Gzodet, and Kapetia have intervened on the aggressor\'s behalf.', 
                          'The senate is in ruin.', 
                          'The historic cities of Aprovotsk, Asentrov, Bfaden, Danhaf, Hfemiz, Lapensk, Shafiq, Strntov, and Ybavgrsbtny are under assault.',
                          'The major port city of Mhortizhskoe along the Gulf of Qair is being bombarded.',
                          '***',
                          '***',
                          'May 2 1980, Qair seized the Strntov Corridor, Southern Mhortizhskoe (Tblirra) and the town of Hafadrah.',
                          '***',
                          '***',
                          'May 18 1980, The Qairi Army has been pushed out of the Opremezh Region of Prankutostan.',
                          '***',
                          '***',
                          'January 24 1981, Prankutostan formally surrenders to Qair. The city of Mhortinzhskoe is partitioned into Tblirra (South) and North Mhortinzhskoe. A buffer zone has been put in place.',
                          'We will never let go of the Strntov Corridor.',
                          'The Prankut people have suffered throughout these years of international suppression.',
                          'We condemn this ethnic marginalization. Together, we must rise up to defend Prankutostan from the invaders.',
                          'All Hail Prankutostan!']

    const currentTranscript = [
        '#########################',
        'March 11 2013 at 11:26 AM, a bomb exploded at the Khia embassy in Hafahdra, Tblirra near the Qair/Prankutostan border.',
        'The free-passage agreement (“Qair-Prankutostan Right to Passage and Free Trade”) between Qair and Prankutostan has been broken. Borders are militarized.',
        'Tensions have been brewing up between Prankutostan and Qair for years after the annexation of the Strntov-Tblirra Corridor in 1981.',
        'However, the implications of Prankutostan orchestrating the attack would cause international scandals.',
        '***',
        '***',
        'At 4:02 PM, the Qairi military started building up their military along the Qair/Prankut buffer zone.',
        'The Qairi Department of Security indicates a group of militants of unknown origin orchestrated the attack.',
        'Gang members and terrorist organizations in major cities near Tblirra-Mhortinzhskoe have been audited, yet the bomb was considered too sophisticated for these organizations to hold.',
        'According to civilians, the lastest evidence of the perpetrators\' presence was the slogan: “Za lyudej Prankuta! Za nas! Za podavlennykh!” - “За людей Пранкута! За нас! За подавленных!” - “For the Prankut People! For Us! For the Suppressed!”',
        'In Snzaq and the Norovia province in Qair, a faction called SRSQ (“Sovereign Republic of Snzaq and Qair”) has been gaining influence over the reigon.',
        'The Prankutostan Intelligence Department supplied the Qair Intelligence Ministry with surveillance footage of neighboring cities.',
        'As an intelligence officer for Qair, you oversee the surveillance footage of neighbouring cities.'
    ]

    let totalDelay = 0;
    const delayTimePerCharacter = 90

    function playTranscript() {
        const transcript = document.getElementsByClassName('transcript')[0];
        prologueMessages.forEach((message) => {
            message.split('').forEach((char, i) => {
                const delay = delayTimePerCharacter * i + Math.floor(Math.random() * 90);
                setTimeout(() => {
                    transcript.textContent += char.toUpperCase();
                }, totalDelay + delay);
            });

            // Add a break line after the message finishes typing
            const messageDuration = delayTimePerCharacter * message.length + 500; // buffer time
            setTimeout(() => {
                transcript.textContent += '\n\n\n';
            }, totalDelay + messageDuration);

            totalDelay += messageDuration + 500; // delay before next message
        });

        const transcriptCurrent = document.getElementsByClassName('transcript-current')[0];
        currentTranscript.forEach((message) => {
            message.split('').forEach((char, i) => {
                const delay = delayTimePerCharacter * i + Math.floor(Math.random() * 90);
                setTimeout(() => {
                    transcriptCurrent.textContent += char;
                }, totalDelay + delay);
            });

            // Add a break line after the message finishes typing
            const messageDuration = delayTimePerCharacter * message.length + 500; // buffer time
            setTimeout(() => {
                transcriptCurrent.textContent += '\n\n';
            }, totalDelay + messageDuration);

            totalDelay += messageDuration + 500; // delay before next message
        });
    }
</script>
<div id="title-container">
    <canvas id="backgroundgl"></canvas>
    <div id="title">Time <span style="font-family: 'Special Elite';">&</span> <span style="font-family: 'Wix Madefor Text'">Conflict</span></div>
    <div id="subtitle"><mark id="highlight-mark">By Dmitri Wamback</mark></div>
</div>
<div id="information">
    <div id="information-box" class="left-information">
        <div style="display: block; width: 100%; height: 100%">
            <div id="information-title">Time in Sherlock Holmes</div>
            <div id="quote">“</div>
            <div id="sub-quote">At present it is not too much to say that it is of such weight it may have an <span class="highlight">influence upon European history.</span></div>
            <div id="sub-quote">A scenario in which time is the ultimate decision of the outcome. Collusion between Sherlock Holmes and the King of Bohemia underlines the narrow thread that peace is dictated by a select-few individuals, whether bureaucratic leaders or detectives.</div>
        </div>
    </div>
    <div id="information-box" class="right-information">
        <div class="europe-map"></div>
    </div>
</div>
<div id="information">
    <div id="information-box" class="right-information">
        <div class="arrival-map"></div>
    </div>
    <div id="information-box" class="left-information">
        <div style="display: block; width: 100%; height: 100%">
            <div id="information-title" style="font-family: 'Wix Madefor Text'">Tensions in <span style="font-style: italic;">Arrival</span></div>
            <div id="quote">“</div>
            <div id="sub-quote" style="font-family: 'Wix Madefor Text'; text-align:center"><span class="highlight">Use Weapon.</span></div>
            <div id="sub-quote" style="font-family: 'Wix Madefor Text'">A scenario in which global tensions are exaserbated therein. Unlike in Scandal in Bohemia, the pressure of world peace is made public, and leaders and the populace are made aware of the international upheaval. Tensions in <span style="font-style: italic;">Arrival</span> highlight the importance of political partnership during times of uncertainty and global disputes.</div>
        </div>
    </div>
</div>
<div id="information">
    <div id="information-box" class="left-information">
        <div style="display: block; width: 100%; height: 100%">
            <div id="information-title" style="font-family: 'Special Elite'">Ethnic marginalization and colonialization in <span style="font-style: italic;">The Wizard of Oz</span></div>
            <div id="quote">“</div>
            <div id="sub-quote" style="font-family: 'Special Elite'; text-align:center">Only <span class="highlight">bad witches are ugly.</span></div>
            <div id="sub-quote" style="font-family: 'Special Elite'">A scenario where the right to freedom of expression is oppressed, setreotypes circulate, and hate speech is common amongst the kakistocracy. Ethnic marginalization and the underlying imperialism in <span style="font-style: italic;">The Wizard of Oz</span> illustrate the neglect on human life based on nationality, appearence, or stereotypes.</div>
        </div>
    </div>
    <div id="information-box" class="right-information">
        <div class="europe-map"></div>
    </div>
</div>
<div id="information">
    <div id="information-box" class="right-information">
        <div style="width: 100%; height: calc(100% - 200px); display: block">
            <div id="part-5"></div>
            <div id="part-4"></div>
            <div id="part-2"></div>
            <div id="part-3"></div>
        </div>
    </div>
    <div id="information-box" class="left-information">
        <div style="display: block; width: 100%; height: 100%; overflow: hidden">
            <div id="information-title" style="font-family: 'Wix Madefor Text'; margin-bottom: 10px">Meet <span style="font-style: italic;">Tblirra Crisis</span>,</div>
            <div id="information-title" style="display: block; text-align: left; font-family: 'Wix Madefor Text'; margin: auto; margin-bottom: 50px; margin-top: 10px; font-size: 20px; width: calc(50vw - 100px); height: auto;">a scenario, set in the fictional nations of Qair (Кяйр | جمهورية إلكير) and Prankutostan (برانكوتوستان | პრანკუტოსტან | Пранкутостан) in March of 2013, that blends the detective and time-constrained aspects of “A Scandal in Bohemia”, international tensions in <span style="font-style: italic;">Arrival</span>, and ethnic marginalization / colonialization in <span style="font-style: italic;">The Wizard of Oz</span>.</div>
            <div id="button-hover" style="width: 300px; padding-top: 20px; padding-bottom: 20px; border-bottom: 2px solid rgb(67, 65, 63); border-right: 2px solid rgb(67, 65, 63); text-align: center; font-size: 20px; margin: auto; margin-top: 50px; margin-bottom: 50px" onclick="{playTranscript()}">Begin Transcript</div>
            <div style="font-family: 'Special Elite'; text-align:left; white-space: pre-line; width: calc(50vw - 100px); margin: auto; word-wrap: break-word;" class="transcript"> </div>
            <div style="font-family: 'Wix Madefor Text'; text-align:left; white-space: pre-line; width: calc(50vw - 100px); margin: auto; word-wrap: break-word;" class="transcript-current"> </div>
        </div>
    </div>

    <script defer>
    </script>    
</div>