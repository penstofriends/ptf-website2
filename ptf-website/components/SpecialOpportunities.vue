<template>
        <section id="section__SpecialOpportunities">
                <h2>Special Opportunities</h2>
                <div class="cards">
                        <OpportunityCard class="opportunityCard" 
                        header="Happy Hearts Indonesia" 
                        img="happyhearts.jpg"
                        description="Happy Hearts Indonesia works with schools in low-income communities to ensure that students can attend a safe school. Happy Hearts uses its funding to build schools and provide educational resources to children in Indonesia."
                        link="https://www.instagram.com/p/CtZMwgmt38J/" 
                        />
                        <div class="stayTuned">
                                <h3>More opportunities to come... stay tuned!</h3>
                        </div>
                </div>
        </section>
</template>
      
<style scoped>
#section__SpecialOpportunities {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        width: 100vw;
        margin-top: 6rem;
}

.cards {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
}

.opportunityCard {
        margin: 1rem;
}

.stayTuned {
        width: 26rem;
        height: 35rem;
        background-color: #fff;
        border-radius: 1rem;
        box-shadow: 0 0.2rem 0.45rem rgba(0, 0, 0, 0.1);
        padding: 0.2rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
}

h3 {
        color: #35312B;
        text-align: center;
        font-size: 1.5rem;
        font-family: 'Montserrat', sans-serif;
        font-weight:600;
        margin-top: 1rem;
        width: 20rem;
        letter-spacing: 0.02rem;
        line-height: 2.25rem;
}

h2 {
        font-family: 'Montserrat', sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 3rem;
        line-height: 3.6875rem;
        color: #35312B;
        margin-top: 6rem;
}
</style>
      