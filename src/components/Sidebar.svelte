<div class="sidebar">
    <h1>art gallery</h1>
    <h2 class="page-title">Home</h2>
    <div class="about">
        <h2>About</h2>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores
            inventore quidem fuga repellendus eligendi dolorem ut nobis
            doloremque ex modi cum, excepturi, qui iste quo enim labore debitis
            tempora vitae?
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
        font-size: 1rem;
        border-right: 2px solid #081c15;
        margin-top: 50px;
        margin-left: 30px;
        position: fixed;
        display: flex;
        flex-direction: column;
        width: 300px;
    }

    .page-title {
        color: #dea19c;
        text-decoration: none;
        margin-bottom: 30px;
        cursor: default;
    }

    .page-title:hover {
        text-decoration: line-through;
    }

    .about {
        border-radius: 10px;
        background-color: #7fd1b9;
        padding: 10px 15px 40px 15px;
        box-shadow: 0px 0px 3px 0px rgba(0, 0, 0, 0.25);
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
            /* border: 1px solid red; */
            /* border: 2px solid red; */
        }
    }
</style>
