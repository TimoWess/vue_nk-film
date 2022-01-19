<template>
  <div className="About">
            <section className="About__title">
                <div>
                    <h1>About</h1>
                    <p>
                        Wir begegnen uns auf Augenhöhe. Pflegen die
                        Partnerschaft. Sind mutig und freundlich.
                    </p>
                </div>
            </section>
            <section className="About__content__wrapper">
                <Profile
                    name="Nils Krebs"
                    position="CEO"
                    description="Voller Fokus: Geschäftsführer und Gründer Nils Krebs führt als Regisseur und Kameramann unsere nationalen und internationalen Produktionen durch. Aufgrund seiner langjährigen Tätigkeit als Art Director bei der Wige Media AG, leitet er zudem unsere Postproduktion."
                    secondDescription="Consectetur adipiscing elit. Aliquam iaculis sit amet enim ac sagittis. Curabitur eget leo varius, elementum mauris eget, egestas quam."
                    image="img/team/team-1.jpg"
                />
                <Profile
                    name="Tobias Paul"
                    position="HEAD OF MARKETING"
                    description="Mit Liebe zum Detail: Tobias Paul kümmert sich um die sorgfältige Planung und den reibungslosen Ablauf unserer Projekte im In- und Ausland. Zudem zeichnet er sich für Marketing und Vertrieb zuständig. Dabei profitiert Tobias von seiner beruflichen Vergangenheit bei der BMW Group, wo er sich ein großes branchenübergreifendes Netzwerk aufbauen konnte."
                    secondDescription="Consectetur adipiscing elit. Aliquam iaculis sit amet enim ac sagittis. Curabitur eget leo varius, elementum mauris eget, egestas quam."
                    image="img/team/team-2.jpg"
                />
                <Profile
                    name="Raphael Schmidt"
                    position="EDITOR"
                    description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vehicula sit amet enim ac sagittis. Curabitur eget leo varius, elementum mauris eget, egestas quam. Donec ante risus, dapibus sed lectus non, lacinia vestibulum nisi. Morbi vitae augue quam. Nullam ac laoreet libero."
                    secondDescription="Consectetur adipiscing elit. Aliquam iaculis sit amet enim ac sagittis. Curabitur eget leo varius, elementum mauris eget, egestas quam."
                    image="img/team/team-3.jpg"
                />
                <Profile
                    name="Charly Spilker"
                    position="SOCIAL MEDIA MANAGER"
                    description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vehicula sit amet enim ac sagittis. Curabitur eget leo varius, elementum mauris eget, egestas quam. Donec ante risus, dapibus sed lectus non, lacinia vestibulum nisi. Morbi vitae augue quam. Nullam ac laoreet libero."
                    secondDescription="Consectetur adipiscing elit. Aliquam iaculis sit amet enim ac sagittis. Curabitur eget leo varius, elementum mauris eget, egestas quam."
                    image="img/team/team-2.jpg"
                />
            </section>
        </div>
</template>

<script>
import Profile from "@/components/Profile.vue"

export default {
  name: "About",
  components: {
    Profile,
  }
}
</script>
