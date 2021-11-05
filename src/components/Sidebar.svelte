<main>
    <div class="header">
        <div class="logo">
            <img src="icons/sau-logo.svg" alt="Southern Adventist University Logo" />
        </div>

        <div class="title">
            <h1>STUDENT MISSIONS</h1>
            <div class="tagline">
                <div>DISCOVER <br /> YOUR PURPOSE</div>
            </div>
        </div>
    </div>

    <div class="facts">
        <h2>Fast Facts</h2>
        <div id="current">
            <img src="icons/serving-ic.svg" />
            <h3>121</h3>
            <p>Students Serving</p>
        </div>
        <div id="countries">
            <img src="icons/countries-ic.svg" />
            <h3>26</h3>
            <p>Countries</p>
        </div>
    </div>

    <div class="commission">
        <p>
            Go into all nations
            <br />
            <span class="verse">
                &mdash; Matt 28:19
            </span>
        </p>
    </div>

    <div class="explore">
        <h2>EXPLORE</h2>
        <div>
            <a href="opportunites.html">Opportunities</a>
            <a href="current.html">Current SMs</a>
            <a href="contact.html">Contact an SM</a>
        </div>
    </div>

    <div class="interest">
        <h2>INTERESTED?</h2>
        <p>Tap to learn more</p>
        <button
            id="sidebar-popover-btn"
            tabindex="0"
            class="btn" 
            role="button" 
            data-bs-toggle="popover" 
            data-bs-trigger="manual"
            data-bs-placement="top"
            data-bs-html="true"
            data-bs-content="<img src='images/learn-qr.svg' />"
        >STUDENT MISSIONS</button>
    </div>
</main>

<style lang="scss">
    main {
        display: flex;
        height: 100vh;
        flex-flow: column nowrap;
        justify-content: space-between;
        background-color: white;
        z-index: 5;
    }

    .logo {
        display: flex;
        width: 100%;
        justify-content: center;
        align-items: center;
        padding: 1rem;
    }

    .title {
        position: relative;
        width: 100%;

        h1 {
            text-align: center;
            padding: .75rem 0;
            margin: 0;
            background-color: var(--lime);
            color: var(--blue);
            position: absolute;
            top: 0;
            left: 0;
            width: 110%;
            text-transform: uppercase;
            font-size: 2vh;
            font-family: 'helveticaneue_condensedCnBd';

            &::after {
                content: '';
                position: absolute;
                top: 100%;
                right: 0;
                width: 0;
                height: 0;
                border-top: 40px solid var(--green);
                border-right: 75px solid transparent;
                z-index: -1;
            }
        }
    }

    .tagline {
        display: flex;
        justify-content: center;
        width: 100%;
        background: var(--blue);
        color: var(--white);
        margin: 0;
        padding: 6vh 1vw 2vh 1vw;
        font-size: 2vh;
        line-height: 1;
        text-transform: uppercase;
        font-family: 'helveticaneue_thincondCnRgTh';

    }

    .facts {
        width: 100%;
        padding: 1rem 1rem 1rem;
        color: var(--blue);
        text-align: center;
        font-family: 'helveticaneue_thincondCnRgTh';

        h2 {
            font-size: 2rem;
            font-family: 'Helvetica 65 Medium';
        }

        h3 {
            font-size: 6vh;
            margin: 0;
            line-height: 1;
            font-weight: 200;
        }

        p {
            color: var(--creamsicle);
            margin: 0;
            font-size: 2vh;
        }

        img {
            height: 2.5rem;
            margin-bottom: 10px;
            padding-right: .25px;
        }

        div {
            position: relative;
            padding: 1rem 0 1rem;

            &::after {
                content: '';
                width: 65%;
                height: 1px;
                background: var(--lGrey);
                position: absolute;
                bottom: 0;
                left: 17%;
            }
        }
    }

    .commission {
        text-align: right;
        color: var(--blue);
        padding: 0 1rem;
        
        span {
            display: inline-block;
            font-size: 1.5vh;
            line-height: 1;
            font-weight: 700;
            font-style: italic;
            font-family: 'helveticaneue_roman';
        }

        p {
            font-size: 3.2vh;
            line-height: 1;
            position: relative;
            z-index: 2;
            padding-left: 20px;
            font-weight: 200;
            font-family: 'Helvetica 35 Thin';

            &::before {
                content: "";
                background: url(../images/qm.png) no-repeat;
                width: 30px;
                height: 40px;
                background-size: 100%;
                position: absolute;
                top: 0;
                left: 0;
                z-index: -1;
            }
        }
    }

    .explore {
        width: 100%;
        border-top: 1px solid var(--lGrey);
        padding: 1rem;

        h2 {
            text-transform: uppercase;
            color: var(--dGrey);
            font-size: 1rem;
            text-align: center;
        }

        a {
            text-decoration: none;
            text-align: right;
            color: var(--dGrey);
            background: rgb(240,240,240);
            font-size: 1.7vh;
            display: block;
            width: 100%;
            padding: .5rem 1.5rem .5rem 0;
            position: relative;
            margin-top: 5px;

            &::after {
                content: url(../icons/arrow.svg);
                width: 8px;
                height: 1.2vh;
                position: absolute;
                right: .5rem;
            }
        }
    }

    .interest {
        width: 100%;
        background: var(--lime);
        text-align: center;
        padding: 1rem;
        color: var(--white);

        h2 {
            color: var(--white);
            font-size: 2.5vh;
            margin-bottom: 0;
        }

        button {
            background: var(--green);
            width: 100%;
            color: var(--white);
            text-decoration: none;
            font-size: 1.5vh;
            padding: .5rem;
            display: block;
            transition: .2s;

            &:hover {
                color: #fff;
                filter: brightness(0.9);
            }
        }
    }
</style>