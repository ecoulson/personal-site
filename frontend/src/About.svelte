<section class="about">
    <div class="about-header">
        <h1 class="about-header-text">About Me</h1>
    </div>
    <div class="about-content">
        <div class="profile-picture-container">
            <img class="profile-picture" alt="Profile shot of Evan Coulson" src="./assets/me.jpg" />
        </div>
        <div class="about-me-text">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed molestie, nisl at suscipit ullamcorper, ante diam blandit ipsum, quis fringilla mauris mauris et leo. Suspendisse tortor elit, congue at eleifend vestibulum, egestas in risus. Duis eleifend felis dolor, sit amet lobortis odio lacinia vitae. Ut semper ipsum turpis, eget ultricies dui fringilla non. Etiam ut lacus a magna convallis dictum vitae at neque. Morbi pharetra lectus ut urna efficitur, vitae placerat velit faucibus. Etiam quis feugiat turpis. Cras viverra a lorem et iaculis. Donec tellus est, posuere at turpis sit amet, porttitor tristique massa. Vivamus justo mi, mollis ut sagittis et, vulputate ut felis. Nam a mattis sapien, non sodales tortor. In id pretium purus. Aliquam vestibulum ligula blandit dictum dignissim. Mauris malesuada bibendum ligula, vel accumsan mi suscipit ac. Proin ac sagittis lectus. Suspendisse potenti.</p>
            <p>Nullam facilisis malesuada ante, et sollicitudin orci malesuada id. Donec nibh neque, porta vitae arcu non, condimentum posuere tortor. Integer vulputate, orci quis lobortis dignissim, dui eros faucibus felis, et placerat nibh enim sed turpis. Aenean ac turpis eu diam tincidunt consectetur. Quisque quis arcu in ipsum scelerisque tincidunt at sed leo. Aliquam nec massa ac diam condimentum elementum. Aliquam faucibus odio vitae dapibus egestas. Aenean ac finibus tortor. Ut at orci lacinia, efficitur purus at, ultricies lacus. Donec rhoncus nulla justo, sagittis blandit risus dictum eu. Praesent commodo ante at enim cursus, id finibus elit lobortis. Curabitur tincidunt nisl ante, eget suscipit ante egestas ut. Vivamus justo lorem, euismod ullamcorper arcu tincidunt, consequat accumsan ante.</p>
        </div>
    </div>
</section>

<style>
    .about {
        grid-area: about;
        box-sizing: border-box;
    }
    .about-content {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    }
    .about-header-text {
        font-size: 64px;
        font-size: clamp(48px, 5vw, 64px);
        text-align: left;
        margin: 0;
        padding-left: 25px;
        text-decoration: underline;
    }   
    .profile-picture-container {
        padding: 15px;
        display: flex;
        box-sizing: border-box;
        justify-content: center;
        align-items: center;    
    }
    .profile-picture {
        display: block;
        border-radius: 100%;
        width: 100%;
        max-width: 250px;
        height: 250px;
        object-fit: cover;
        border: 3px solid #84828F;
    }
    .about-me-text {
        padding: 15px;
        box-sizing: border-box;
    }
    .about-me-text {
        font-size: 16px;
        font-size: clamp(14px, 1vw, 16px);
    }
</style>