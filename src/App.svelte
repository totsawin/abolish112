<script>
  import { Temporal } from 'proposal-temporal/lib/index.mjs';
  const todayDate = Temporal.now.plainDateISO();
  const people = [
	  {
		  name: `จตุภัทร์ บุญภัทรรักษา "ไผ่ดาวดิน"`,
		  nickname: 'pai',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 3, day: 8 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 4, day: 23 }),
			  },
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 8, day: 11 }),
			  }
		  ]
	  },
	  {
		  name: `พริษฐ์ ชิวารักษ์ "เพนกวิน"`,
		  nickname: 'penguin',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 2, day: 9 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 11 }),
			  },
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 8, day: 9 }),
			  }
		  ]
	  },
	  {
		  name: `ภาณุพงศ์ จาดนอก "ไมค์"`,
		  nickname: 'mike',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 3, day: 8 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 6, day: 1 }),
			  },
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 8, day: 9 }),
			  }
		  ]
	  },
	  {
		  name: `สมยศ พฤกษาเกษมสุข`,
		  nickname: 'somyot',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 2, day: 9 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 4, day: 23 }),
			  }
		  ]
	  },
	  {
		  name: `อานนท์ นำภา`,
		  nickname: 'arnon',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 2, day: 9 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 6, day: 1 }),
			  },
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 8, day: 11 }),
			  }
		  ]
	  },
	  {
		  name: `ปติวัฒน์ สาหร่ายแย้ม "หมอลำแบงค์"`,
		  nickname: 'bank',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 2, day: 9 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 4, day: 9 }),
			  }
		  ]
	  },
	  {
		  name: `ปนัสยา สิทธิจิรวัฒนกุล "รุ้ง"`,
		  nickname: 'rung',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 3, day: 8 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 6 }),
			  }
		  ]
	  },
	  {
		  name: `อัญชัน (สงวนนามสกุล)`,
		  nickname: 'anchan',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 1, day: 19 }),
			  }
		  ]
	  },
	  {
		  name: `ไชยอมร แก้ววิบูลย์พันธุ์ "แอมมี่ เดอะ บอตทอมบลูส์"`,
		  nickname: 'ammy',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 3, day: 4 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 11 }),
			  }
		  ]
	  },
	  {
		  name: `ปริญญา ชีวินกุลปฐม "พอร์ท วงไฟเย็น"`,
		  nickname: 'port',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 3, day: 6 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 12 }),
			  }
		  ]
	  },
	  {
		  name: `ปิยรัฐ จงเทพ “โตโต้”`,
		  nickname: 'toto',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 3, day: 6 }),
				releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 5 }),
			  }
		  ]
	  },
	  {
		  name: `พรหมศร วีระธรรมจารี "ฟ้า"`,
		  nickname: 'fah',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 3, day: 17 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 10 }),
			  },
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 8, day: 9 }),
			  }
		  ]
	  },
	  {
		  name: `ชูเกียรติ แสงวงค์ "จัสติน"`,
		  nickname: 'justin',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 3, day: 23 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 6, day: 2 }),
			  }
		  ]
	  },
	  {
		  name: `ธวัช สุขประเสริฐ`,
		  nickname: 'tawat',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 2, day: 24 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 18 }),
			  }
		  ]
	  },
	  {
		  name: `ศักดิ์ชัย ตั้งจิตสดุดี`,
		  nickname: 'sakchai',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 2, day: 24 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 13 }),
			  }
		  ]
	  },
	  {
		  name: `ฉลวย เอกศักดิ์`,
		  nickname: 'chaluay',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 2, day: 24 }),
		 		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 13 }),
			  }
		  ]
	  },
	  {
		  name: `ณัฐนนท์ ไชยมหาบุตร`,
		  nickname: 'frank',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 2, day: 24 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 18 }),
			  }
		  ]
	  },
	  {
		  name: `สิรภพ พุ่มพึ่ง`,
		  nickname: 'kanoon',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 6 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 9 }),
			  }
		  ]
	  },
	  {
		  name: `หทัยรัตน์ แก้วสีคราม`,
		  nickname: 'ploy',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 2 }),
		 		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 10 }),
			  }
		  ]
	  },
	  {
		  name: `พรชัย`,
		  nickname: 'pornchai',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 3, day: 11 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 4, day: 22 }),
			  }
		  ]
		  
	  },
	  {
		  name: `วรรณวลี ธรรมสัตยา`,
		  nickname: 'tee',
		  detainedDuration: [
			  {
				detainedDate: Temporal.PlainDate.from({ year: 2021, month: 4, day: 27 }),
		  		releasedDate: Temporal.PlainDate.from({ year: 2021, month: 5, day: 7 }),
			  }
		  ]
	  },
  ]

  function getNumberOfDaysUnderDetained(detainedDuration) {
	return detainedDuration.reduce((acc, {detainedDate, releasedDate = todayDate} ) =>
		acc + detainedDate.until(releasedDate, { largestUnit: 'days' }).days, 
		0
	);
  }
</script>

<div class="people">
	{#each people as individual}
		<div class="individual">
			<div class="individual__title">
				{ individual.name }
			</div>
			<div class="individual__name">      
				<span>{getNumberOfDaysUnderDetained(individual.detainedDuration)} วัน ถูกคุมขังโดยไม่ได้รับการประกันตัว</span>
			</div>
			<div class="individual__image">
				<picture>
					<source srcset="./assets/{individual.nickname}.avif" type="image/avif">
					<source srcset="./assets/{individual.nickname}.webp" type="image/webp">
					<img src="./assets/{individual.nickname}.jpg" loading=”lazy” alt="{individual.name}"/>
				  </picture>
				{#if individual.detainedDuration[individual.detainedDuration.length - 1].releasedDate}
					<div class="stamp is-bailed">ประกันตัว</div>
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
    column-gap: 10px;
    row-gap: 20px;
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
    grid-template-rows: 10% 5% auto;
  }

  .individual__title {
    align-items: center;
    display: grid;
    font-size: 1.5em;
    font-weight: bold;
	padding-left: 1rem;
	border-bottom: 1px solid;
  }

  .individual__name {
	/* background-color: #ddb0e1; */
    color: #f9f2e2;
    align-items: center;
    display: grid;
    font-size: 1em;
	padding-left: 1rem;
	border-bottom: 1px solid;
  }

  .individual__image {
	position: relative;
	background-color: #98d6f7;
	overflow: hidden;
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
