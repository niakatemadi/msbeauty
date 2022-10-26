<template>
    <div class="Tableau">
        <section class="Tableau-inner">
            <h3 @click="displayinfo(1)">Les sourcils </h3>
            <table cellspacing="0" v-if="displayInfo==1">
                <tr><td>Epilation sourcils</td><td class="Tableau-price">15€<br/><span>30min</span></td></tr>
                <tr><td>Epilation sourcils + Teinture</td><td class="Tableau-price">20€<br/><span>30min</span></td></tr>
            </table>
            <h3 @click="displayinfo(2)">Forfaits</h3>
            <table cellspacing="0" v-if="displayInfo==2">
                <tr><td>Forfait Verni Semi-Permanent</td><td class="Tableau-price">50€<br/><span>1h10</span></td></tr>
                <tr><td>Forfait Gel X + Vernis Semi-Permanents Pieds</td><td class="Tableau-price">60€<br/><span>1h40</span></td></tr>
                <tr><td>Forfait Manucure russe + Pédicure russe avec vsp renforcé</td><td class="Tableau-price">90€<br/><span>2h30</span></td></tr>
            </table>
            <h3 @click="displayinfo(3)">Forfaits Cils et Sourcils Yumi</h3>
            <table cellspacing="0" v-if="displayInfo==3">
                <tr><td>Soin Brow Lift + Yumi Lashes</td><td class="Tableau-price">95€<br/><span>1h30</span></td></tr>
            </table>
            <h3 @click="displayinfo(4)">Soin Sourcils Complet YumiBrows</h3>
            <table cellspacing="0" v-if="displayInfo==4">
                <tr><td>Brow Lift + Epilation + Teinture Sourcils + Soin Kératine et protéines</td><td class="Tableau-price">40€<br/><span>45min</span></td></tr>
            </table>
            <h3 @click="displayinfo(5)">Beauté du Regard</h3>
            <table cellspacing="0"  v-if="displayInfo==5">
                <tr><td>Yumilashes</td><td class="Tableau-price">70€<br/><span>1h20</span></td></tr>
                <tr><td>Yumilashes Offre Duo</td><td class="Tableau-price">120€<br/><span>1h45</span></td></tr>
                <tr><td>Yumibrows</td><td class="Tableau-price">60€<br/><span>1h</span></td></tr>
                <tr><td>Yumilashes + Yumibrows</td><td class="Tableau-price">110€ <br/><span>1h45</span></td></tr>
                <tr><td>Henna Brows</td><td class="Tableau-price">110€<br/>30€<br/><span>1h</span></td></tr>
            </table>
            <h3 @click="displayinfo(6)">Beauté des Pieds</h3>
            <table cellspacing="0" v-if="displayInfo==6">
                <tr><td>Vernis Semi-Permanent Couleur</td><td class="Tableau-price">29€<br/><span>40min</span></td></tr>
                <tr><td>Dépose + nouvelle pose vernis semi-permanent Couleur </td><td class="Tableau-price">34€<br/><span>45min</span></td></tr>
                <tr><td>Pédicure russe avec vsp</td><td class="Tableau-price">50€<br/><span>1h</span></td></tr>
                <tr><td>Pédicure russe sans vernis</td><td class="Tableau-price">25€<br/><span>30min</span></td></tr>
                <tr><td>Supplément French</td><td class="Tableau-price">5€<br/><span>10min</span></td></tr>
                <tr><td>Supplément baby-boomer</td><td class="Tableau-price">15€<br/><span>15min</span></td></tr>
                <tr><td>Dépose seule<br/>Retrait du verni semi permanent sans repose de verni</td><td class="Tableau-price">10€<br/><span>30min</span></td></tr>
                <tr><td>Vernis Perméable Halal<br/>Vernis simple qui laisse passer l'eau</td><td class="Tableau-price">20€<br/><span>30min</span></td></tr>
                <tr><td>Spa Seul</td><td class="Tableau-price">25€<br/><span>30min</span></td></tr>
                <tr><td>YumiFeet Seul</td><td class="Tableau-price">35€<br/><span>30min</span></td></tr>
                <tr><td>Supplément Vernis</td><td class="Tableau-price">5€<br/><span>10min</span></td></tr>
                <tr><td>Supplément Vernis Semi-Permanent</td><td class="Tableau-price">10€<br/><span>15min</span></td></tr>
                <tr><td>Réparation 1 ongle (Gros orteil)</td><td class="Tableau-price">3€<br/><span>10min</span></td></tr>
                <tr><td>Réparation 2 ongles</td><td class="Tableau-price">5€<br/><span>15min</span></td></tr>
            </table>
            <h3 @click="displayinfo(7)" >Les Cils</h3>
            <table cellspacing="0" v-if="displayInfo==7">
                <tr><td>Réhaussement De Cils Avec Teinture</td><td class="Tableau-price">45€<br/><span>1h</span></td></tr>
                <tr><td>Extension Cils A Cils</td><td class="Tableau-price">70€<br/><span>2h</span></td></tr>
                <tr><td>Retouche Extension</td><td class="Tableau-price">50€<br/><span>1h30</span></td></tr>
                <tr><td>Extension De Cils Mixte</td><td class="Tableau-price">90€<br/><span>2h</span></td></tr>
                <tr><td>Retouche Extension Mixte</td><td class="Tableau-price">70€<br/><span>1h30</span></td></tr>
            </table>
            <h3 @click="displayinfo(8)" >Maquillage Semi Permanent Visage</h3>
            <table cellspacing="0"  v-if="displayInfo==8">
                <tr><td>Ras De Cils</td><td class="Tableau-price">150€<br/><span>1h</span></td></tr>
                <tr><td>Première Retouche Ras De Cils</td><td class="Tableau-price">A définir<br/> <span>1h</span></td></tr>
                <tr><td>Retouche Ras De Cils Un An</td><td class="Tableau-price">90€<br/><span>1h</span></td></tr>
                <tr><td>Taches De Rousseur</td><td class="Tableau-price">70€<br/><span>45min</span></td></tr>
                <tr><td>Retouche Tache De Rousseur</td><td class="Tableau-price">50€<br/><span>30min</span></td></tr>
                <tr><td>Grain De Beauté</td><td class="Tableau-price">30€<br/><span>15min</span></td></tr>
            </table>
            <h3 @click="displayinfo(9)">Réhaussement De Cils</h3>
            <table cellspacing="0" v-if="displayInfo==9" >
                <tr><td>Réhaussement De Cils Classique Avec Teinture</td><td class="Tableau-price">45€<br/><span>1h</span></td></tr>
                <tr><td>Réhaussement Yumi Lashes</td><td class="Tableau-price">65€<br/><span>1h15</span></td></tr>
            </table>

            <h3 @click="displayinfo(10)" >Kit Press-On Nails</h3>
            <table cellspacing="0" v-if="displayInfo==10">
                <tr><td>Finition Couleur</td><td class="Tableau-price">49€<br/><span>15min</span></td></tr>
                <tr><td>Finition French</td><td class="Tableau-price">54€<br/><span>15min</span></td></tr>
                <tr><td>Finition Baby-Boomer</td><td class="Tableau-price">59€<br/><span>15min</span></td></tr>
            </table>
        </section>
    </div>
</template>
<script>
  export default {
    name: "aboutView",
    data() {
        return {
            displayInfo : 0
        };
    },
    methods: {
        displayinfo(number) {
            this.displayInfo = number;
        }
    }
};
  </script>
<style scoped>
.Tableau {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 100px;
    background: rgba(192,192,192,1);
    color: rgba(187,34,179,1);
    font-weight: bold;
}
.Tableau-inner{
    box-shadow: 0px 0px 15px rgba(187,34,179,1);
    background-color: rgba(255,255,255,0.2);
    margin-right : 5px;
    margin-left:5px;
}
.Tableau-price{
    text-align:end;
    padding-right:10px;
}
span {
    color :rgb(137, 19, 131);
    font-size: smaller;
}
table {
    width : 100%;
    background-color: rgba(187,34,179,0.2);
}
td{
    color:black;
    border-bottom : 1px solid black;
}
h3{
    text-align: center;
    text-decoration: underline;
    margin:0;
    padding-top:15px;
    height: 40px;
    border-bottom:2px solid rgb(137, 19, 131);
}
h3:hover {
    cursor:pointer;
}
</style>