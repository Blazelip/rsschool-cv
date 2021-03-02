# CV

## Name:
Filyukov Dmitry

## Contacts:
Mail: filin1994@rambler.ru
Telegram: @scepticson

# A few fords about me:
I'm 26 y.o. ex. digital-marketer last time working in the sphere of CPA. For 7 years I passed through the way of freelance, advertising agency owner and independent affiliate. Traffic and clicks were my religion, but from the childhood I got the dream to be a programmer. So now it's time to make it real.

# Skills:
- HTML
- CSS (SCSS/LESS)
- BEM methodology
- Crossbrowsing/Adaptive layout
- Javascript (Vanilla)
- Git (Github)
- Gulp / Webpack

# Code examples

```javascript

const makePin = (offerData) => {
  if (offerData.offer === ``) {
    return null;
  }

  const node = pinTemplate.cloneNode(true);
  const pinImg = node.querySelector(`img`);

  node.dataset.id = `${offerData.offer.id}`;
  node.style.left = `${offerData.location.x - PIN_WIDTH / 2}px`;
  node.style.top = `${offerData.location.y - PIN_HEIGHT}px`;
  pinImg.src = offerData.author.avatar;
  pinImg.alt = offerData.offer.title;

  return node;
};

const renderPins = (offers) => {
  const fragment = document.createDocumentFragment();

  offers.forEach((offer) => {
    const currentPin = makePin(offer);
    if (currentPin) {
      fragment.appendChild(currentPin);
    }

  });

  pinBoard.appendChild(fragment);
};

const deletePins = () => {
  const pins = pinBoard.querySelectorAll(`.map__pin:not(.map__pin--main)`);

  pins.forEach((pin) => {
    pin.remove();
  });
};

const onPinClick = (evt) => {
  const target = evt.target;

  if (target.tagName === `IMG` || target.classList.contains(`map__pin`)) {

    if (!target.classList.contains(`map__pin--main`) && !target.closest(`.map__pin--main`)) {
      const id = parseInt(target.dataset.id, 10);
      const number = id ? id : parseInt(evt.target.closest(`.map__pin`).dataset.id, 10);

      const offer = window.dataWithId.find((item) => {
        return item.offer.id === number;
      });

      if (offer) {
        removeActiveClass();
        const pin = target.closest(`.map__pin`);
        pin.classList.add(`map__pin--active`);
        window.card.show(offer);
      }
    }
  }
};

```

# Experience
Graduated HTML Academy profession "Front-end Developer". While studying made 4 projects. 
- [Device](https://github.com/Blazelip/79521-device-28) - online store 
- [Mishka](https://github.com/Blazelip/79521-mishka-20) - online store
- [Code and Magic](https://github.com/Blazelip/Code-and-magick) - simple Javascript game
- [Keksobooking](https://github.com/Blazelip/79521-keksobooking-21) - Javascript for booking service

After that, at non-paid Internship I've done 3 simple landings with minimal Javascript features.
- [Trip to Europe](https://github.com/Blazelip/europe) - landing for travel agency
- [Bicycles](https://github.com/Blazelip/cycles) - landing for online store of bicycles
- [Smart Device](https://github.com/Blazelip/printing) - landing for online microchip store

# Education:
Actually I've got a bachelor degree in economics, but my last job was connected with online-marketing and advertising.
I don't have any degree in Computer Sciense. Only HTML Academy Courses.

# English: 
I could say that I got B2 level in speaking, and a little worse in writing/reading, especcially in professional subjects.

