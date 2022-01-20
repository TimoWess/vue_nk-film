<template>
  <div className="Services">
            <section className="Services__title center-item">
                <h1>Services</h1>
            </section>
            <section className="Services__content__wrapper">
                <div className="Services__content__header">
                    <h2>Unser Vision. Unsere Leidenschaft.</h2>
                    <p>Der perfekte Film für sie!</p>
                </div>
                <hr />
                <div className="Services__content__main wrapper">
                    <div className="Services__content">
                        <i className="fas fa-lightbulb center-item"></i>
                        <h3>KONZEPTION</h3>
                        <p>
                            Die wichtigste Phase der Filmerstellung. Mit einem
                            schlüssigen und stichhaltigen Konzept kann schon
                            fast nichts mehr schiefgehen. Wir erstellen das
                            perfekt auf sie zugeschnittene Konzept oder stehen
                            ihnen zur Seite, wenn sie diesen Schritt selbst
                            vornehmen wollen.
                        </p>
                    </div>
                    <div
                        className="Services__content"
                        style="--delay: 0.4s"
                    >
                        <i className="fas fa-film center-item"></i>
                        <h3>DREHARBEITEN</h3>
                        <p>
                            Hier spielen wir all unsere Stärken aus: über ein
                            Jahrzehnt Erfahrung, grenzenlose Kreativität gelernt
                            auf Produktionen auf der ganzen Welt, technisches
                            Know-How, ein Netzwerk an hochprofessionellen
                            Spezial-Kräften, technische Dienstleister der
                            Spitzenklasse und vor allem immer eine positive und
                            freundschaftliche Arbeitsatmosphäre.
                        </p>
                    </div>
                    <div
                        className="Services__content"
                        style="--delay: 0.6s"
                    >
                        <i className="fas fa-cog center-item"></i>
                        <h3>POSTPRODUKTION</h3>
                        <p>
                            Hier entsteht die Magie. Nichts ist unmöglich, so
                            scheint es. Und dieser Satz kommt der Wahrheit schon
                            sehr nahe. Egal ob kunst- und gefühlvoller Schnitt,
                            Animationen, Overlays, 3D-Tracking, Augmented oder
                            Virtual Reality - wir setzen alle anfallenden
                            Postproduktions-Schritte direkt inhouse für sie um.
                            Damit wird sich ihr Film spür- und sichtbar von der
                            Masse unterscheiden - und damit ein besonderes
                            Highlight in ihrer Unternehmenspräsentation und
                            Außendarstellung.
                        </p>
                    </div>
                </div>
                <div className="waves1" ref={waves}></div>
            </section>
            <section className="Services__examples">
                <div className="eg wrapper">
                    <div className="eg__image">
                        <img src="@/assets/img/red.png" alt="camera" />
                    </div>
                    <div className="eg__text">
                        <div className="eg__title">
                            <h2>High-End Kameratechnik</h2>
                            <hr />
                        </div>
                        <div className="eg__description">
                            <p>
                                Verschiedene Einsatzzwecke erfordern
                                unterschiedliche Herangehensweisen. Wir beraten
                                Sie gerne, welche Kamera zu ihrem Vorhaben
                                passt.
                            </p>
                            <p>
                                Es muss nicht immer Kino-Kameratechnik sein,
                                aber ein iPhone reicht meist auch nicht aus.
                                Durch unsere pragmatische Herangehensweise und
                                die individuellen Anforderungen ihrer
                                Filmproduktion finden wir immer den besten und
                                wirtschaftlich sinnvollsten Weg für unsere
                                Partner!
                            </p>
                            <button
                                className="btn--filled"
                                style="--pad: 0.5em"
                            >
                                ANGEBOT EINHOLEN
                            </button>
                        </div>
                    </div>
                </div>
            </section>
        </div>
</template>

<script>
export default {

}
</script>

<style>

</style>