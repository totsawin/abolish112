<script>
  const todayDate = new Date();
  const MILLISECONDS = 1000;
  const SECONDS = 60;
  const MINUTES = 60;
  const HOURS = 24;
  const DAYS_IN_MS = HOURS * MINUTES * SECONDS * MILLISECONDS;
  const people = [
	  {
		  name: `Jatupat 'Pai Dao Din' Boonpatraksa`,
		  detainedDate: new Date(2021, 2, 8),
		  releasedDate: new Date(2021, 3, 23),
		  isBailed: true,
	  },
	  {
		  name: `Parit 'Penguin' Chiwarak`,
		  detainedDate: new Date(2021, 1, 9),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Panupong 'Mike' Jadnok`,
		  detainedDate: new Date(2021, 2, 8),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Somyot Pruksakasemsuk`,
		  detainedDate: new Date(2021, 1, 9),
		  releasedDate: new Date(2021, 3, 23),
		  isBailed: true,
	  },
	  {
		  name: `Arnon Nampa`,
		  detainedDate: new Date(2021, 1, 9),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Patiwat Saraiyaem, 'Mor Lam Bank'`,
		  detainedDate: new Date(2021, 1, 9),
		  releasedDate: new Date(2021, 3, 9),
		  isBailed: true,
	  },
	  {
		  name: `Panusaya Sithijirawattanakul`,
		  detainedDate: new Date(2021, 2, 8),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Anchan (family name withheld)`,
		  detainedDate: new Date(2021, 0, 19),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Chaiamorn 'Ammy' Kaewwiboonpan`,
		  detainedDate: new Date(2021, 2, 4),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Parinya Cheewin Kulpathom aka 'Port Faiyen'`,
		  detainedDate: new Date(2021, 2, 6),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Piyarat 'Toto' Jongthep`,
		  detainedDate: new Date(2021, 2, 6),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Promsorn Viradhammajari`,
		  detainedDate: new Date(2021, 2, 17),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Chukait Saengwong aka 'Justin'`,
		  detainedDate: new Date(2021, 2, 23),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Tawat Sukpraseat`,
		  detainedDate: new Date(2021, 1, 24),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Sakchai Tangchitsadudi`,
		  detainedDate: new Date(2021, 1, 24),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
	  {
		  name: `Chaluay Ekkasit`,
		  detainedDate: new Date(2021, 1, 24),
		  releasedDate: todayDate,
		  isBailed: false,
	  },
  ]
  function getNumberOfDaysUnderDetained(detainedDate, releasedDate) {
    return Math.floor((releasedDate - detainedDate) / DAYS_IN_MS);
  }
</script>

<div class="people">
	{#each people as individual, index}
		<div class="individual">
			<div class="individual__title">
				{ individual.name }
			</div>
			<div class="individual__name">      
				<span>{getNumberOfDaysUnderDetained(individual.detainedDate, individual.releasedDate)} Days Held Under Trial</span>
			</div>
			<div class="individual__image">
				<picture>
					<source srcset="./assets/{index + 1}.avif" type="image/avif">
					<source srcset="./assets/{index + 1}.webp" type="image/webp">
					<img src="./assets/{index + 1}.jpg" loading=”lazy” alt="{individual.name}"/>
				  </picture>
				{#if individual.isBailed}
					<div class="stamp is-bailed">Bailed</div>
				{/if}	
			</div>
  		</div>
	{/each}	  
</div>

<style>
  :global(body) {
    /* this will apply to <body> */
    background-color: black;
    margin: 0;
  }

  .people {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    grid-column-gap: 0.5rem;
    grid-row-gap: 1rem;
  }

  .individual {
    position: relative;
    width: 100%;
    margin: 0 auto;
	background-color: #4a4a4a;
    color: #fff;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
    display: grid;
    font-family: "helvetica", "arial", sans-serif;
    grid-template-areas:
      "title"
      "name"
      "image";
    grid-template-rows: 10% 5% auto;
  }

  .individual__title {
    align-items: center;
    display: flex;
    font-size: 1.5em;
    font-weight: bold;
	padding-left: 1rem;
	border-bottom: 1px solid;
    grid-area: title;
  }

  .individual__name {
	/* background-color: #ddb0e1; */
    color: #f9f2e2;
    align-items: center;
    display: flex;
    font-size: 1em;
	padding-left: 1rem;
	border-bottom: 1px solid;
    grid-area: name;
  }

  .individual__image {
	position: relative;
	background-color: #98d6f7;
	overflow: hidden;
    grid-area: image;
	text-align: center;
  }

  img {
    /* bottom: -2em;
    left: -3em; */
    width: 100%;
	height: 100%;
  }

  .stamp {
	font-weight: 700;
	text-transform: uppercase;
	mix-blend-mode: multiply;
	position: absolute;
	top: 50%;
	transform: translate(-50%, -50%);
}

.is-bailed {
	color: #C4C4C4;
	border: 1rem double #C4C4C4;
	transform: rotate(-5deg);
	font-size: 6rem;
	font-family: "Open sans", Helvetica, Arial, sans-serif;
	border-radius: 0;
	padding: 0.5rem;
} 
</style>
