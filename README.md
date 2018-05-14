# chess-with-tony
<br>

Chess with Tony is a website that was commissioned by Tony Niccoli, an independent children’s chess teacher in West London looking to expand his reach and provide a platform to disseminate information to his customers. 

Tony was looking for a simple, static-looking website, but one that he could update periodically without the need for any coding. Additionally, Tony did not want to use an external CMS like WP, Drupal etc. which left me with a dilemma, as It was impractical for me to be kept on retainer to maintain the site going forward. After looking into a PHP/Laravel back-end setup, I settled on creating a simple NodeJS app that would use MongoDB to create a simple, free CMS that Tony could make posts and receive enquiries.

After further research I found KeystoneJS, a Node-based open-source CMS that handles the backend, but allows the front-end to be customised. Keystone employs the Yeoman generator that, through NPM, installs a ‘blank’ version of Keystone complete with view templates and models ready to launch. I opted to use Handlebars instead of the default Jade templating engine. 

However, the current version of Keystone is somewhat outdated, and most packages in the package.json file needed to be updated at the outset, and crucially, the CMS came loaded with Bootstrap 3, not 4. Updating Bootstrap was the most time-consuming of these initialisation processes but was by no means unachievable. 

Once the setup was complete, customising the .hbs templates formed the basis of my work, and was a simple case of incorporating the data parsed from the models into the templates and then styling accordingly. 

KeystoneJS is an extremely convenient open-source ‘plug in and play’ CMS that is easily customisable, should you not require anything not outlined in the original Yeoman build. The downside of Keystone is that it is frightfully inflexible should you wish to add anything to site which involves the Keystone backend. In particular, .pdf files cannot be embedded by someone (i.e. my client) using the CMS without digging through reams of Javascript in the Keystone Node-Modules folder that is currently beyond my ability. 

Overall, and for the most basic blog-style websites, I would wholly recommend KeystoneJS as quick and free solution to creating a dynamic website. I would caution though, anyone wishing to incorporate more complex features via the CMS backend as it is very difficult to add a feature without bringing the house of cards down. 
