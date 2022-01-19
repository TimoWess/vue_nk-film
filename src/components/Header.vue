<template>
  <header className="Header" id="Header">
            <div className="Header__wrapper wrapper">
                <router-link to="/" id="header__logo" onClick={goTop}>
                    <img src={logo} alt="" />
                </router-link>
                <div className="Header__link__container">
                    {/* eslint-disable-next-line */}
                    <ul role="list">
                        <li className="center-item">
                            <router-link
                                to="/"
                                className="
                                    
                                "
                                onClick={goTop}
                            >
                                HOME
                            </router-link>
                        </li>
                        <li className="center-item">
                            <router-link
                                to="/about"
                                className=""
                                onClick={goTop}
                            >
                                ABOUT
                            </router-link>
                        </li>
                        <li className="center-item">
                            <router-link
                                to="/services"
                                className=""
                                onClick={goTop}
                            >
                                SERVICES
                            </router-link>
                        </li>
                        <li className="center-item">
                            <router-link
                                to="/work"
                                className=""
                                onClick={goTop}
                            >
                                WORK
                            </router-link>
                        </li>
                        <li className="center-item">
                            <router-link
                                to="/contact"
                                className=""
                                onClick={goTop}
                            >
                                CONTACT
                            </router-link>
                        </li>
                        <li className="center-item">
                            <a href="https://www.facebook.com">
                                <div className="center-item">
                                    <i className="fab fa-facebook"></i>
                                </div>
                            </a>
                        </li>
                        <li className="center-item">
                            <a href="https://www.twitter.com">
                                <div className="center-item">
                                    <i className="fab fa-twitter"></i>
                                </div>
                            </a>
                        </li>
                        <li className="center-item">
                            <a href="https://www.linkedin.com">
                                <div className="center-item">
                                    <i className="fab fa-linkedin"></i>
                                </div>
                            </a>
                        </li>
                    </ul>
                </div>
                <div className="Header__link__container--mobile">
                    {/* <div className="Header__link__social"> */}
                    <a href="https://www.facebook.com">
                        <div>
                            <i className="fab fa-facebook"></i>
                        </div>
                    </a>
                    <a href="https://www.twitter.com">
                        <div>
                            <i className="fab fa-twitter"></i>
                        </div>
                    </a>
                    <a href="https://www.linkedin.com">
                        <div>
                            <i className="fab fa-linkedin"></i>
                        </div>
                    </a>
                    {/* </div> */}
                    <button
                        className="Header__link__btn"
                        onClick={() => {
                            darkener.current.style.visibility = "visible";
                            darkener.current.style.opacity = "0.5";
                            mobileMenu.current.style.left = "50%";
                        }}
                    >
                        <i className="fas fa-bars"></i>
                    </button>
                    <div
                        className="Header__link__darkener"
                        ref="darkener"
                        style={{ opacity: 0 }}
                        v-on:click="hideMobileNav(false)"
                    ></div>
                    <div
                        className="Header__link__wrapper--mobile"
                        ref="mobileMenu"
                    >
                        {/* eslint-disable-next-line */}
                        <ul role="list">
                            <li>
                                <router-link
                                    to="/"
                                    className=""
                                    v-on:click="hideMobileNav(true)"
                                >
                                    <div>HOME</div>
                                </router-link>
                            </li>
                            <li>
                                <router-link
                                    to="/about"
                                    className=""
                                    v-on:click="hideMobileNav(true)"
                                >
                                    <div>ABOUT</div>
                                </router-link>
                            </li>
                            <li>
                                <router-link
                                    to="/services"
                                    className=""
                                    v-on:click="hideMobileNav(true)"
                                >
                                    <div>SERVICES</div>
                                </router-link>
                            </li>
                            <li>
                                <router-link
                                    to="/work"
                                    className=""
                                    v-on:click="hideMobileNav(true)"
                                >
                                    <div>WORK</div>
                                </router-link>
                            </li>
                            <li>
                                <router-link
                                    to="/contact"
                                    className=""
                                    v-on:click="hideMobileNav(true)"
                                >
                                    <div>CONTACT</div>
                                </router-link>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </header>
</template>

<script>
export default {
	methods: {
		hideMobileNav(goTop) {
        this.$refs.mobileMenu.style.left = "100%";
        this.$refs.darkener.style.opacity = "0";
        if (goTop) window.scrollTo(0, 0);
        setTimeout(() => {
            this.$refs.darkener.style.visibility = "hidden";
        }, 300);
    },

    goTop() {
        window.scrollTo(0, 0);
    }
	}
}
</script>

<style>

</style>