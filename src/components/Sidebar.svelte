<div class="sidebar">
    <h1 class="header">art gallery</h1>
    <h2 class="page-title">Home</h2>
    <div class="years-links">
        <h2>Year Directory</h2>
        <a href="#2021" class="years-link"> 2021 </a>
        <a href="#2020" class="years-link"> 2020 </a>
    </div>
    <div class="about">
        <h2>About</h2>
        <p>
            A place to document in-progress or finished art projects. Loading
            time is being worked on.
        </p>
        <p class="about-subsection">
            Click/tap on pictures to see them full-size.
        </p>
    </div>
    <div class="mobile-support-message">
        <p>
            Mobile support is not 100% supported yet. Expect some things to look
            weird.
        </p>
    </div>
</div>

<style>
    .sidebar {
        display: flex;
        flex-direction: column;
        flex: 1;
        text-align: right;
        padding: 0px 25px 35px 10px;
        height: 150px;
        border-right: 2px solid #081c15;
        margin-top: 50px;
        margin-left: 30px;
        position: fixed;
        display: flex;
        flex-direction: column;
        width: 300px;
    }

    .header {
        font-size: 3.5em;
    }

    .page-title {
        color: #dea19c;
        text-decoration: none;
        margin-bottom: 20px;
        cursor: default;
        font-size: 1.75em;
    }

    .page-title:hover {
        text-decoration: line-through;
    }

    .about {
        border-radius: 10px;
        background-color: #7fd1b9;
        padding: 10px 15px 40px 15px;
        -webkit-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
        -moz-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
        box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
    }

    .mobile-support-message {
        margin-top: 15px;
        text-align: center;
        background-color: #ecb0e1;
        height: 80px;
        padding: 10px;
        border-radius: 10px;
        -webkit-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
        -moz-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
        box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
    }

    .about-subsection {
        margin-top: 20px;
    }

    .years-links {
        display: flex;
        flex-direction: column;
        margin-bottom: 25px;
    }

    .years-link {
        text-decoration: none;
        font-size: 1.5em;
        color: #dea19c;
        cursor: pointer;
    }

    .years-link:hover {
        text-decoration: line-through;
    }

    @media screen and (max-device-width: 1100px) {
        .sidebar {
            border: none;
            width: 90%;
            position: relative;
            margin: 50px 0px 0px 0px;
            padding: 5px;
            justify-content: right;
            height: auto;
        }

        .mobile-support-message {
            height: 45px;
        }
    }
</style>
