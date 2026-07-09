<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>WishHaus UAE</title>

<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#120734;color:white}
a{text-decoration:none;color:inherit}
nav{position:fixed;top:0;width:100%;z-index:99;display:flex;justify-content:space-between;padding:18px 6%;background:rgba(18,7,52,.65);backdrop-filter:blur(14px)}
nav a{margin:0 10px;font-weight:bold}
.brand{color:#ffd76a;font-size:22px}

section{min-height:100vh;padding:110px 6% 60px}
.hero{display:grid;place-items:center;text-align:center;background:radial-gradient(circle,#6e4cff,#26105c,#080216)}
h1{font-size:clamp(42px,8vw,86px);color:#ffd76a;text-shadow:0 0 25px #ff9;margin:10px 0}
h2{font-size:32px}
p{font-size:19px;line-height:1.6;color:#efe7ff}
.btn,button{display:inline-block;margin:8px;padding:14px 22px;border-radius:999px;border:1px solid rgba(255,255,255,.25);background:rgba(255,255,255,.12);color:white;font-weight:bold;cursor:pointer}
.primary{background:linear-gradient(90deg,#ffd76a,#ff8bd1);color:#220735}

.house{width:220px;height:220px;margin:auto;position:relative;filter:drop-shadow(0 0 35px #ffd76a);animation:float 4s infinite ease-in-out;cursor:pointer}
.roof{position:absolute;left:18%;top:0;width:64%;height:50%;background:linear-gradient(135deg,#ffd76a,#ff8bd1);clip-path:polygon(50% 0,100% 100%,0 100%);display:grid;place-items:center;font-size:40px}
.body{position:absolute;left:22%;top:45%;width:56%;height:50%;background:#eadcff;border:4px solid #ffd76a;border-radius:18px}
.door{position:absolute;bottom:0;left:38%;width:24%;height:48%;background:#5e2bc8;border-radius:12px 12px 0 0}
.window{position:absolute;top:25%;width:18%;height:18%;background:#8ff;border-radius:50%;box-shadow:0 0 18px #8ff}
.w1{left:18%}.w2{right:18%}
@keyframes float{50%{transform:translateY(-16px)}}

.kingdom{background:linear-gradient(#1b0c52,#42156d,#10051f)}
.map{position:relative;min-height:760px;border-radius:36px;background:radial-gradient(circle,#5c36c9,#1d0b50 65%);border:1px solid rgba(255,255,255,.18)}
.center{position:absolute;left:50%;top:50%;transform:translate(-50%,-50%);text-align:center}
.center .house{width:120px;height:120px}
.island{position:absolute;width:190px;min-height:130px;padding:20px;border-radius:35px;background:rgba(255,255,255,.16);backdrop-filter:blur(12px);box-shadow:0 20px 40px rgba(0,0,0,.25);text-align:center}
.island span{font-size:38px;display:block}
.island small{display:block;color:#eee}

.i0{left:8%;top:10%}.i1{left:36%;top:5%}.i2{right:8%;top:12%}.i3{left:5%;top:38%}
.i4{right:6%;top:38%}.i5{left:14%;bottom:9%}.i6{left:38%;bottom:4%}.i7{right:15%;bottom:10%}
.i8{left:57%;top:19%}.i9{left:24%;top:25%}.i10{right:26%;bottom:24%}.i11{left:42%;top:36%}

.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:22px}
.card,.box,.result{background:rgba(255,255,255,.11);border:1px solid rgba(255,255,255,.16);border-radius:28px;padding:24px}
.poster{height:220px;border-radius:25px;background:linear-gradient(135deg,#ffd76a,#ff8bd1,#8a7dff);display:grid;place-items:center;font-size:80px}
.theme-page{display:none}
.two{display:grid;grid-template-columns:1fr 1fr;gap:24px}
.pill{background:rgba(255,255,255,.12);padding:14px 18px;border-radius:18px}
input,textarea{width:100%;padding:15px;margin:8px 0;border-radius:15px;border:0}
textarea{min-height:120px}

@media(max-width:800px){
nav{position:static;display:block}
.map{min-height:auto;padding:20px}
.center,.island{position:static;transform:none;margin:14px auto}
.two{grid-template-columns:1fr}
}
</style>
</head>

<body>

<nav>
<a class="brand" href="#home">🏠 WishHaus UAE</a>
<div>
<a href="#kingdom">Kingdom</a>
<a href="#themes">Themes</a>
<a href="#quiz">Not Sure?</a>
<a href="#booking">Book</a>
</div>
</nav>

<section id="home" class="hero">
<div>
<div onclick="location.href='#kingdom'" class="house">
<div class="roof">✦</div><div class="body"><div class="door"></div><div class="window w1"></div><div class="window w2"></div></div>
</div>
<h1>Welcome To WishHaus</h1>
<h2>Every Wish Begins With A Story</h2>
<p>Beyond the stars, above the clouds, lies a magical world where dreams become adventures and celebrations become unforgettable memories.</p>
<a class="btn primary" href="#kingdom">✨ Enter The House Of Wishes</a>
<a class="btn" href="#quiz">Not Sure Which Theme?</a>
</div>
</section>

<section id="kingdom" class="kingdom">
<h1>Choose Your Adventure</h1>
<p>The WishHaus door has opened. Follow a magical path and discover the celebration made for your child.</p>
<div class="map" id="map"></div>
</section>

<section id="themes">
<h1>Discover Every Adventure</h1>
<p>Each theme has its own story, activities, and magical world.</p>
<div class="grid" id="themeGrid"></div>
</section>

<section id="themeDetails"></section>

<section id="quiz">
<h1>Not Sure Which Adventure To Choose?</h1>
<p>Let the WishHaus magic guide you.</p>
<div class="box">
<button onclick="recommend('superhero')">Hero & Action</button>
<button onclick="recommend('mermaid')">Ocean Magic</button>
<button onclick="recommend('ice-princess')">Royal Princess</button>
<button onclick="recommend('enchanted-unicorn')">Fantasy Magic</button>
<button onclick="recommend('dinosaur')">Dinosaur Adventure</button>
<button onclick="recommend('barbie')">Fashion & Glam</button>
<button onclick="recommend('gardening')">Nature</button>
<button onclick="recommend('kpop-hunter')">Music & Stars</button>
<button onclick="recommend('slimetastic')">Slime Fun</button>
</div>
<div id="quizResult"></div>
</section>

<section id="booking">
<h1>Start Your Adventure</h1>
<form class="box" action="mailto:wishhausuae@gmail.com" method="post" enctype="text/plain">
<input name="Parent Name" placeholder="Parent Name">
<input name="Child Name" placeholder="Child Name">
<input name="Child Age" placeholder="Child Age">
<input name="Preferred Theme" placeholder="Preferred Theme">
<input name="Preferred Date" placeholder="Preferred Date">
<input name="Number of Children" placeholder="Number of Children">
<textarea name="Special Requests" placeholder="Special Requests"></textarea>
<button class="primary">Send Booking Request</button>
</form>
<p>Email: wishhausuae@gmail.com<br>WhatsApp: +971 56 851 3087</p>
</section>

<script>
const themes=[
{slug:"mermaid",title:"Mermaid Adventure Party",emoji:"🧜",place:"Mermaid Lagoon",tagline:"Dive Into Ocean Magic!",story:"Step beneath the waves and discover an enchanting underwater world filled with shimmering treasures, colorful sea creatures, and magical adventures.",activities:["Mermaid Tail Crafting","Ocean Slime Lab","Seashell Crown Decorating"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Mermaid Performer — AED 1,600","Magic & Illusion Show — AED 800"]},
{slug:"slimetastic",title:"Slimetastic Party",emoji:"🧪",place:"Slime Laboratory",tagline:"The Ultimate Slime Adventure!",story:"A colorful, stretchy, squishy world where children mix, create, and customize slime masterpieces.",activities:["Slime Mixing Workshop","Glitter Slime Creation","Custom Slime Decorating"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"dinosaur",title:"Dinosaur Adventure Party",emoji:"🦕",place:"Dino Jungle",tagline:"Journey Back To The Age Of Dinosaurs!",story:"A prehistoric adventure where young explorers discover ancient creatures and dinosaur-sized fun.",activities:["Dinosaur Mask Crafting","Fossil Slime Lab","Dinosaur Egg Decorating"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"ice-princess",title:"Ice Princess Party",emoji:"❄️",place:"Ice Kingdom",tagline:"Enter A Magical Winter Kingdom!",story:"A sparkling world of icy wonders, snowflake magic, and royal adventures.",activities:["Snowflake Crown Crafting","Frozen Slime Lab","Princess Wand Decorating"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"barbie",title:"Barbie Dream Party",emoji:"🎀",place:"Barbie Boulevard",tagline:"A World Of Pink Perfection!",story:"A glamorous celebration of fashion, friendship, creativity, and confidence.",activities:["Barbie Crown Crafting","Pink Sparkle Slime Lab","Fashion Accessory Decorating"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"hello-kitty",title:"Hello Kitty Party",emoji:"🐱",place:"Hello Kitty Town",tagline:"Sweetness & Smiles!",story:"A charming world filled with friendship, adorable crafts, and delightful activities.",activities:["Hello Kitty Headband Crafting","Sweet Slime Lab","Charm Bracelet Decorating"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"enchanted-unicorn",title:"Enchanted Unicorn Party",emoji:"🦄",place:"Unicorn Valley",tagline:"Follow The Rainbow!",story:"A whimsical land where unicorns, rainbows, sparkles, and imagination come together.",activities:["Unicorn Headband Crafting","Rainbow Slime Lab","Magic Wand Decorating"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"gardening",title:"Gardening Party",emoji:"🌱",place:"Secret Garden",tagline:"Plant, Create & Grow!",story:"A nature-inspired hands-on gardening adventure for young creators.",activities:["Flower Pot Painting","Mini Planting Workshop","Garden Marker Decorating"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"kpop-hunter",title:"K-Pop Hunter Party",emoji:"⭐",place:"K-Pop Stage",tagline:"Shine Like A K-Pop Star!",story:"A star-worthy celebration filled with music, creativity, style, and performance fun.",activities:["Idol Photo Card Decorating","K-Pop Slime Lab","Star Badge Creation"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"labubu",title:"Labubu Adventure Party",emoji:"🎨",place:"Labubu Village",tagline:"A Playful World Of Fun!",story:"A whimsical celebration packed with creativity, surprises, and playful adventures.",activities:["Labubu Tote Bag Decorating","Labubu Slime Lab","Character Keychain Crafting"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"spiderman",title:"Spiderman Adventure Party",emoji:"🕷️",place:"Spider City",tagline:"Swing Into Action!",story:"A superhero adventure where young heroes tackle challenges and discover their inner powers.",activities:["Spider Mask Crafting","Web Slime Lab","Spider Hero Badge Creation"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]},
{slug:"superhero",title:"Superhero Adventure Party",emoji:"🦸",place:"Hero City",tagline:"Unleash Your Inner Hero!",story:"An action-packed celebration where young heroes train, create, and complete exciting missions.",activities:["Superhero Mask Crafting","Superhero Slime Lab","Hero Power Badge Creation"],upgrades:["Full Balloon Backdrop & Standee — AED 500","Standard Balloon Setup — AED 300","Face Painting — AED 300","Magic & Illusion Show — AED 800"]}
];

const map=document.getElementById("map");
map.innerHTML=<div class="center"><div class="house"><div class="roof">✦</div><div class="body"><div class="door"></div><div class="window w1"></div><div class="window w2"></div></div></div><strong>The House of Wishes</strong></div>;
themes.forEach((t,i)=>{
map.innerHTML+=<a class="island i${i}" href="#themeDetails" onclick="showTheme('${t.slug}')"><span>${t.emoji}</span><b>${t.place}</b><small>${t.tagline}</small></a>;
});

const grid=document.getElementById("themeGrid");
themes.forEach(t=>{
grid.innerHTML+=<div class="card" onclick="showTheme('${t.slug}');location.href='#themeDetails'"><div class="poster">${t.emoji}</div><h3>${t.title}</h3><p>${t.tagline}</p><button>Explore</button></div>;
});

function showTheme(slug){
const t=themes.find(x=>x.slug===slug);
document.getElementById("themeDetails").innerHTML=`
<h1>${t.title}</h1>
<h2>${t.tagline}</h2>
<p>${t.story}</p>
<p><b>Duration:</b> 2 Hours &nbsp; <b>Rate:</b> 145 AED per Child</p>
<div class="two">
<div class="box"><h2>What’s Included</h2>${t.activities.map(a=><p class="pill">✨ ${a}</p>).join("")}</div>
<div class="box"><h2>Upgrade The Experience</h2>${t.upgrades.map(u=><p class="pill">🎈 ${u}</p>).join("")}</div>
</div>
<div class="box"><h2>The Ultimate Celebration Awaits!</h2><p>Food and drinks are not included. A 50% deposit is required to secure the booking.</p><a class="btn primary" href="#booking">✨ Begin This Adventure</a></div>`;
}

function recommend(slug){
const t=themes.find(x=>x.slug===slug);
document.getElementById("quizResult").innerHTML=<div class="result"><h2>${t.emoji} ${t.title}</h2><p>${t.story}</p><a class="btn primary" href="#themeDetails" onclick="showTheme('${t.slug}')">View This Adventure</a></div>;
}
</script>

</body>
</html>
