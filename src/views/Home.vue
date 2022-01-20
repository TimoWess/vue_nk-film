<template>
  <div className="Home">
            <section>
                <div className="Home__video__container"></div>
                <div className="Home__content">
                    <p className="Home__dark">
                        <span style="fontSize: 16pt">
                            Unsere Vision. Unsere Leidenschaft
                        </span>
                    </p>
                    <h1 className="Home__dark" style="--delay: 0.2s">
                        <span style="fontSize: 30pt, fontWeight: bold">
                            DEIN WERBE-FILM.
                        </span>
                    </h1>
                    <p>Wir haben keine Kunden, wir haben Partner.</p>
                    <div className="Home__buttons__wrapper">
                        <router-link to="/about">
                            <button
                                className="btn--empty"
                                onClick="goTop"
                            >
                                Mehr über uns!
                            </button>
                        </router-link>
                        <a href="mailto:info@nk-film.de">
                            <button className="btn--filled">
                                Kostenlose Beratung
                            </button>
                        </a>
                    </div>
                </div>
            </section>
            <section className="Home__whatwedo">
                <div className="Home__whatwedo__wrapper wrapper">
                    {/* eslint-disable-next-line */}
                    <ul className="Home__whatwedo__examples" role="list">
                        <li
          
                        >
                            <div className="inner_circle">
                                <i className="fas fa-lightbulb"></i>
                            </div>
                            <h3>Konzeption</h3>
                        </li>
                        <li
                            
                        >
                            <div className="inner_circle">
                                <i className="fas fa-film"></i>
                            </div>
                            <h3>Dreharbeit</h3>
                        </li>
                        <li
                            
                        >
                            <div className="inner_circle">
                                <i className="fas fa-cog"></i>
                            </div>
                            <h3>Postproduktion</h3>
                        </li>
                        <li
                            
                        >
                            <div className="inner_circle">
                                <i className="fas fa-rocket"></i>
                            </div>
                            <h3>Marketing</h3>
                        </li>
                    </ul>
                    <div className="Home__whatwedo__content">
                        <div
                            
                        >
                            <p>
                                Die wichtigste Phase der Filmerstellung. Mit
                                einem schlüssigen und stichhaltigen Konzept kann
                                schon fast nichts mehr schiefgehen. Wir
                                erstellen das perfekt auf sie zugeschnittene
                                Konzept oder stehen ihnen zur Seite, wenn sie
                                diesen Schritt selbst vornehmen wollen.
                            </p>
                        </div>
                        <div
                            
                        >
                            <p>
                                Hier spielen wir all unsere Stärken aus: über
                                ein Jahrzehnt Erfahrung, grenzenlose Kreativität
                                gelernt auf Produktionen auf der ganzen Welt,
                                technisches Know-How, ein Netzwerk an
                                hochprofessionellen Spezial-Kräften, technische
                                Dienstleister der Spitzenklasse und vor allem
                                immer eine positive und freundschaftliche
                                Arbeitsatmosphäre.
                            </p>
                        </div>
                        <div
                            
                        >
                            <p>
                                Hier entsteht die Magie. Nichts ist unmöglich,
                                so scheint es. Und dieser Satz kommt der
                                Wahrheit schon sehr nahe. Egal ob kunst- und
                                gefühlvoller Schnitt, Animationen, Overlays,
                                3D-Tracking, Augmented oder Virtual Reality -
                                wir setzen alle anfallenden
                                Postproduktions-Schritte direkt inhouse für sie
                                um. Damit wird sich ihr Film spür- und sichtbar
                                von der Masse unterscheiden - und damit ein
                                besonderes Highlight in ihrer
                                Unternehmenspräsentation und Außendarstellung.
                            </p>
                        </div>
                        <div
                            
                        >
                            <p>
                                Lassen sie ihren Film nicht im digitalen Nirwana
                                untergehen, sondern lassen sie uns gemeinsam ein
                                perfektes Konzept für die Veröffentlichung
                                erarbeiten.
                            </p>
                        </div>
                    </div>
                    <Link to="services">
                        <button
                            className="btn--empty"
                        >
                            Mehr erfahren!
                        </button>
                    </Link>
                </div>
            </section>
            <div id="pt">
                <video muted playsInline loop>
                    <source src="@/assets/video/showreel.mp4" />
                </video>
            </div>
        </div>
</template>

<script>

export default {
  name: 'Home',
  methods: {
    goTop() {
        window.scrollTo(0, 0);
    },
  }
}
</script>
