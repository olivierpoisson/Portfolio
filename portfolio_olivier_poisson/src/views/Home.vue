<template>
    <section class="hero">
        <div class="web">
            <h1 class="titleWeb">Web</h1>
            <p class="text">
                I love to help compagnies build amazing and attracting websites
                that help them get more customers
            </p>
        </div>
        <img class="heroImg" src="../assets/Heroimage.png" alt="" />
        <div class="software">
            <h1 class="titleSoft">Software</h1>
            <p class="text">
                I love to help compagnies build amazing and functionnal
                softwares so they can give their customers the best experience
                possible
            </p>
        </div>
    </section>
    <section class="section2">
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Consequatur aspernatur labore rem fugit eos repellat ratione
            molestiae harum delectus deserunt non consequuntur, cum, assumenda
            itaque placeat asperiores? Laudantium velit quae accusantium ad?
            Inventore libero laudantium sit molestias odio ullam illo repellat
            animi blanditiis nobis tempore at ad hic ipsam alias aspernatur,
            nesciunt distinctio nulla laboriosam consequuntur, deleniti sed
            autem est delectus! Assumenda est sequi at, quod molestiae aperiam
            eligendi error quaerat natus nisi accusamus, aspernatur ipsam sit id
            illo. Nobis tempora, aut beatae deleniti libero hic necessitatibus
            asperiores inventore architecto aliquid corrupti ratione autem iusto
            facilis, maxime qui odio numquam. Lorem ipsum dolor sit amet,
            consectetur adipisicing elit. Voluptatibus illum laborum, aliquam
            totam fugiat magni quam reprehenderit ex atque omnis architecto
            obcaecati tempore quos ducimus adipisci repudiandae fuga quas odio,
            amet, autem earum rem pariatur molestiae. Sit odio praesentium
            ducimus deleniti ipsam iste quasi iure laudantium, dolorum
            perspiciatis earum libero quas distinctio doloremque? Libero aut
            quibusdam cum nobis nemo officia eveniet ipsa enim qui provident ab
            officiis iure facilis beatae dolores recusandae veritatis excepturi
            saepe, maxime voluptatibus rem dignissimos nesciunt! Vitae possimus
            in quos expedita dolore veritatis, praesentium cum, earum molestias
            consequuntur iure! Ab labore harum enim culpa, possimus nobis omnis
            ut similique facilis facere quas molestiae corrupti cupiditate
            maxime sequi fugiat consequatur laudantium quidem veniam illo,
            perferendis quae beatae cumque! A nobis quaerat maiores maxime. Vero
            voluptates, magni repellat recusandae omnis incidunt esse officiis
            at quibusdam repellendus unde pariatur obcaecati odit totam, autem
            ad a accusamus cupiditate placeat quidem maiores praesentium hic
            possimus! Corporis minima, adipisci officiis doloribus quibusdam
            reprehenderit vel omnis nemo quos rerum illo! Expedita quis hic a
            libero corporis dolorum, accusamus optio iusto autem aut nam dolores
            asperiores nisi nihil suscipit debitis laudantium. Unde a officiis
            veniam fugiat in, enim incidunt itaque veritatis. A incidunt
            distinctio nulla totam, ducimus nihil ex. Eius, voluptatibus
            perspiciatis velit voluptates reprehenderit iste consectetur, nihil
            error a ratione hic quod ullam libero voluptate suscipit soluta
            itaque in natus laborum porro possimus nobis fugit. Culpa et odit
            provident, accusantium laudantium iste quibusdam vero obcaecati sit
            ullam cum sequi nostrum harum iusto voluptatem modi similique,
            molestiae consequatur quaerat fuga ex. Dolor incidunt facere non
            sapiente quibusdam perspiciatis! Aperiam expedita aliquam neque
            veniam vitae, earum consectetur quo odit blanditiis, sit culpa
            laboriosam nulla, dignissimos accusamus. Asperiores quaerat culpa
            vel eius ipsa architecto labore, perferendis sit ab veritatis
            deserunt vero, voluptatem minus dolores porro tenetur! A, minus
            quas! Porro asperiores consequuntur culpa odio maiores voluptate ut
            ex aspernatur officia aliquid, quaerat, eligendi veritatis illo
            possimus, ducimus natus commodi? Facilis fugit aliquam minima illo
            voluptatum accusamus corrupti, voluptates iusto cupiditate. Quod
            pariatur error atque iusto cumque consectetur eligendi
            necessitatibus unde! Iusto quod inventore dignissimos deleniti
            dolore molestiae iste qui nesciunt magnam odit porro sunt optio
            laboriosam quaerat dicta explicabo dolorem fugit doloremque
            praesentium saepe, exercitationem quisquam vero ea! Dolor,
            voluptatem eligendi. Non beatae modi accusantium odio illum
            obcaecati, praesentium hic suscipit fuga! Ducimus dignissimos
            perspiciatis officiis adipisci asperiores autem ab delectus maiores
            ratione consectetur voluptates quos eligendi voluptate natus, odit
            nisi omnis quis dicta repudiandae consequuntur? Dolor corporis fuga,
            neque numquam sed fugit nesciunt dolorem vero omnis necessitatibus
            ea aspernatur magni? At quia quas, accusamus veritatis amet nihil
            optio quam ea pariatur minus eius nulla ullam. Unde delectus
            mollitia, qui architecto nisi exercitationem illum ullam eveniet
            iste laborum quasi veritatis accusantium deserunt obcaecati neque
            dolorum magni tempora perferendis nihil, deleniti reprehenderit! Hic
            totam distinctio deleniti praesentium explicabo, nemo error corporis
            sunt pariatur doloribus delectus sequi unde consequuntur quia sint?
            Velit eius repellendus, ipsa possimus totam quod atque commodi
            quasi. Velit officia quibusdam consequuntur nemo tempora
            accusantium.
        </p>
    </section>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);
export default {
    name: "Home",
    components: {},
    methods: {
        heroScrollAnimation() {
            const timeline = gsap.timeline({
                scrollTrigger: {
                    trigger: ".hero",
                    start: "0%",
                    end: "80%",
                    scrub: true,
                },
            });
            timeline.fromTo(".hero", { opacity: 1 }, { opacity: 0 });
        },
        HeroTextAnimation() {
            const timeline = gsap.timeline({
                defaults: {
                    duration: 1,
                },
            });
            timeline.fromTo(
                ".heroImg",
                { opacity: 0 },
                { opacity: 1, duration: 2, ease: "Power2.easeIn" }
            );
            timeline.fromTo(
                ".titleWeb",
                { x: 50, opacity: 0 },
                { x: 0, opacity: 1, ease: "Power2.easeOut" },
                "<50%"
            );
            timeline.fromTo(
                ".titleSoft",
                { x: -50, opacity: 0 },
                { x: 0, opacity: 1, ease: "Power2.easeOut" },
                "<"
            );
            timeline.fromTo(
                ".text",
                { y: 50, opacity: 0 },
                { y: 0, opacity: 1 },
                "<50%"
            );
        },
        setup() {
            gsap.set(".underline", { width: "0%" });
            gsap.set(".hero", { zIndex: "-1" });
            gsap.set(".section2", { zIndex: "2", position: "relative" });
        },
    },
    mounted: function () {
        this.heroScrollAnimation();
        this.HeroTextAnimation();
    },
};
</script>
<style scoped>
.hero {
    height: 100vh;
    display: flex;
    z-index: 1;
    justify-content: center;
    position: sticky;
    top: 0;
}
.heroImg {
    transform: scale(1.3);
    transform-origin: bottom;
}

.web,
.software {
    display: flex;
    align-items: center;
    flex: 1;
    flex-direction: column;
    padding: 0px 50px;
    justify-content: center;
    overflow: hidden;
}
.titleWeb,
.titleSoft {
    font-size: 4em;
}
.section2 {
    z-index: 2;
    padding: 10vw;
    position: relative;
}
.text {
    color: #4d4b4b;
}
</style>
