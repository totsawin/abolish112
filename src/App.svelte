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
		  detainedDate: new Date(2021, 2, 8)
	  },
	  {
		  name: `Parit 'Penguin' Chiwarak`,
		  detainedDate: new Date(2021, 1, 9)
	  },
	  {
		  name: `Panupong 'Mike' Jadnok`,
		  detainedDate: new Date(2021, 2, 8)
	  },
	  {
		  name: `Somyot Pruksakasemsuk`,
		  detainedDate: new Date(2021, 1, 9)
	  },
	  {
		  name: `Arnon Nampa`,
		  detainedDate: new Date(2021, 1, 9)
	  },
	  {
		  name: `Patiwat Saraiyaem, 'Mor Lam Bank'`,
		  detainedDate: new Date(2021, 1, 9)
	  },
	  {
		  name: `Panusaya Sithijirawattanakul`,
		  detainedDate: new Date(2021, 2, 8)
	  },
	  {
		  name: `Anchan (family name withheld)`,
		  detainedDate: new Date(2021, 0, 19)
	  },
	  {
		  name: `Chaiamorn 'Ammy' Kaewwiboonpan`,
		  detainedDate: new Date(2021, 2, 4)
	  },
	  {
		  name: `Parinya Cheewin Kulpathom aka 'Port Faiyen'`,
		  detainedDate: new Date(2021, 2, 6)
	  },
	  {
		  name: `Piyarat 'Toto' Jongthep`,
		  detainedDate: new Date(2021, 2, 6)
	  },
	  {
		  name: `Prommes`,
		  detainedDate: new Date(2021, 2, 17)
	  },
  ]
  function getNumberOfDaysUnderDetained(detainedDate) {
    return Math.floor((todayDate - detainedDate) / DAYS_IN_MS);
  }
</script>

<div class="people">
	{#each people as individual, index}
		<div class="individual">
			<div class="individual__title">
				{ individual.name }
			</div>
			<div class="individual__name">      
				<span>{getNumberOfDaysUnderDetained(individual.detainedDate)} Days Held Under Trial</span>
			</div>
			<div class="individual__image">
				<img src="./assets/{index + 1}.jpeg" alt="{individual.name}"/>
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
  }

  img {
    /* bottom: -2em;
    left: -3em; */
    width: 100%;
	height: 100%;
  }
</style>
