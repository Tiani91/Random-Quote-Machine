<div class="container-fluid text-center">
  <h1>Random Quote Generator</h1>
  <p>Some of my favorite quotes!</p>
  <button class="btn btn-default" type="submit">New Quote</button>
  <div class="quotes">
    <span class="quote">Death is not the greatest loss in life. The greatest loss is what dies inside us while we live.</span>
    <span class="author">- Norman Cousins</span>
  </div>
  <img src="http://www.encina.se/wp-content/uploads/byro.jpg"/>
</div>
h1{
  color:lightpink;
  font-size: 54px;
}
p{
  color: lightblue;
  font-style:italic;
  font-size: 20px;
  padding: 25px;
}
body{
  background-color:grey;
  font-family: "Times New Roman";
}
img{
  padding:25px;
}

.quotes{
  background-color:black;
  width:50%;
  margin-right:auto;
  margin-left:auto;
  border-color:white;
  border-style:ridge;
  border-width:5px;
  border-radius:5px;
  margin-top:20px;
  padding: 20px;
  height:auto;
  color:white;
  font-size:20px;
}
.author{
  font-size:15px;
  font-style:italic;
}
$(document).ready(function() {

  function getQuote() {
    var quotes = ["The best way to predict the future if to create it.", "We know what we are, but know not what we may be.", "It is during our darkest moments that we must focus to see the light.", "You can't blame gravity for falling in love.", "If you know the enemy and know yourself you need not fear the results of a hundred battles.", "I am become death, the destroyer of worlds."];
    var author = ["- Abraham Lincoln", "- William Shakespeare", "- Aristotle Onassis", "- Albert Einstein", "- Sun Tzu", "- J. Robert Oppenheimer"];
    var randomNum = Math.floor((Math.random() * quotes.length));
    var randomQuote = quotes[randomNum];
    var randomAuthor = author[randomNum];
    $(".quote").text(randomQuote);
    $(".author").text(randomAuthor);

  }
  $(".btn").on("click", function() {
    getQuote();
  });
});
