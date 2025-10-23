# Assignment

## Introduction

Reviews of restaurants are posted in the Yelp's website, `https://www.yelp.com`. As part of your responsibilities as VP of Marketing, you are expected to present a quarterly analysis of the comments some restaurants receive in social media.

The following five examples, formatted as JSON objects, have been extracted from the Yelp page of a popular Spanish restaurant, Socarrat Paella Bar, in New York City's Chelsea neighborhood, `https://www.yelp.com/biz/socarrat-paella-bar-chelsea-new-york-3`.

```
{
	"author": "Essence V.",
	"rating": 5,
	"review": "We celebrated my sister's birthday at this venue. The staff was friendly and made sure we were well taken care of. We had a fantastic time. The portion sizes are generous; contrary to some reviews, I didn't find it expensive. We finished every dish, even when we were already full. My only recommendation is to include sitting for people who may have difficulty using high chairs inside the venue."
}
{
	"author": "Linh N.",
	"rating": 4,
	"review": "We came on a weeknight and there was no wait. We enjoyed the outdoor dining in the back. It was a very romantic setting with string lights and we had the whole backyard to ourselves. Our server was quick and attentive- so happy we weren't forgotten for sitting outside! The paella was very good- there is a thin layer of rice so that gave the rice a sort of crunchy texture at the bottom and soft on top. The only complaint is that the food is on the pricier side.."
}
{
	"author": "Bennett L.",
	"rating": 3,
	"review": "Came here with two other friends; we had originally thought that there was a $32 lunch special (Paella and a Tapa), but found out that it was only for the Midtown location. We ordered the Socarrat Paella and the Croquette. The Paella was solid, though I didn't think it was anything too mind blowing. The portion was ~$34 a person, which I would say is on the pricier side. (Though the portions are pretty generous) As a heads up, the Paella will usually take ~30 minutes to prepare, so would definitely keep this in mind when you're dining here."
}
{
	"author": "Isabel P.",
	"rating": 2,
	"review": "The paella here tasted like trader joes frozen paella, honestly trader joes might have been better. I was really disappointed because the location and ambiance are great, waiter was friendly and helpful as well. I don't know what they're doing wrong with the food but it tasted like watered down frozen scallops and shrimp were heated up in a microwave and served over overcooked rice."
}
{
	"author": "Raj N.",
	"rating": 1,
	"review": "Overpriced and served cold. The photo below is 2 servings of Paella, $76 plus tax and tips. It may look a generous amount, but those seafood are cut in half."
}
```

## Task

The task is to engineer a prompt for a chat app (e.g. ChatGPT, Gemini, etc), that extracts short comments on specific aspects of the customer's experience. The desired format for the output would be a JSON object containing the "author" key and some additional keys, such as "price", "food", "atmosphere", "service" or "dishes_mentioned". The objective is to store all this information in a format that facilitates subsequent analysis.