
# Laravel, I choose you!

As developers we look for tools that help us be as efficient as we can possibly be. On the front end we see this with the rise in the use of frameworks like React, Angular, and Vue for JavaScript. While we have Foundation and Bootstrap for CSS. Frameworks help us build projects and minimize the amount of time it takes to finish those projects. Like JavaScript and CSS, PHP has many frameworks available also, like CodeIgniter, Zend Framework, Cake, Symfony, and SilverStripe, but all of these pale in comparison to Laravel.

I began to learn Laravel about a year ago with the release of 5.2, actually when I was designing this site. At the time I was going through a few courses on Codecademy and Udemy for PHP and at the time was going to build it with basic PHP, but I had a dilemma. I wanted to learn PHP but I didn't want to take 30 years to build the site that would showcase my work and abilities. So I began to look at Frameworks. First I looked at CodeIgniter but it seemed like it was dying and Symfony was way too complicated for me. Then I came across Laravel. Immediately, I began to do research and it became my choice and here's why.

<blockquote>Laravel is a simple framework for web application development. It attempts to make writing web applications in PHP as simple as possible. <br /> - Taylor Otwell *(Creator of Laravel)*</blockquote>


## The Documentation

One of the best features that comes with Laravel is their [documentation](http://www.laravel.com/docs). Let's face it, we all have looked at the docs of other frameworks or APIs and Immediately we're more confused than we were before. As a junior front end developer, who has only a little PHP experience, finding good documentation is like finding gold in the Gold Rush. That's what Laravel is, pure gold.

The Laravel documentation has everything that you would want. It's extensive, clear, has many examples, searchable, and it even comes with a couple of tutorials. The docs take you from it's installation, down into all of it's most important features, and gives examples of how to use them with very accurate detail. I have to say without the Laravel documentation being as clear as it is, Laravel would have been much more difficult to learn, but not impossible, which brings me to my other reasons I chose the framework.

## The Code

Being a developer, you get to build and support some amazing products, but with that also comes the crappy products. If you ever dealt with legacy code from the 90's and early 2000's you'll know what I mean, but Laravel's code and structure does a few things that a good framework should do.

### Standards

Laravel does a very good job following the PSR coding standards, but other than that it almost forces you to do the same. The code is written beautifully. Controllers are and should be separated out for their different functions. Using commands in the terminal, Laravel can create boilerplates for controllers, models, migrations, and more. As a developer, it's not only good to learn a technology but learn how to use that tech properly and follow the guidelines that come along with it, Laravel does that with PHP.

    php artisan make:controller # Makes a controller DUH!

Here's an example of the simple boilerplate it provides:
    <?php

    namespace App\Http\Controllers;

    use Illuminate\Http\Request;

    class ExampleController extends Controller
    {
        //
    }
And here's an example of the CRUD boilerplate:
    <?php

    namespace App\Http\Controllers;

    use Illuminate\Http\Request;

    class ExampleController extends Controller
    {
        /*
         * Display a listing of the resource.
         *
         * @return \Illuminate\Http\Response
         */
        public function index()
        {
            //
        }

        /*
         * Show the form for creating a new resource.
         *
         * @return \Illuminate\Http\Response
         */
        public function create()
        {
            //
        }

        /*
         * Store a newly created resource in storage.
         *
         * @param  \Illuminate\Http\Request  $request
         * @return \Illuminate\Http\Response
         */
        public function store(Request $request)
        {
            //
        }

        /*
         * Display the specified resource.
         *
         * @param  int  $id
         * @return \Illuminate\Http\Response
         */
        public function show($id)
        {
            //
        }

        /*
         * Show the form for editing the specified resource.
         *
         * @param  int  $id
         * @return \Illuminate\Http\Response
         */
        public function edit($id)
        {
            //
        }

        /*
         * Update the specified resource in storage.
         *
         * @param  \Illuminate\Http\Request  $request
         * @param  int  $id
         * @return \Illuminate\Http\Response
         */
        public function update(Request $request, $id)
        {
            //
        }

        /*
         * Remove the specified resource from storage.
         *
         * @param  int  $id
         * @return \Illuminate\Http\Response
         */
        public function destroy($id)
        {
            //
        }
    }*


As you can see this would be a very helpful start.

### Extendable

If there's something you think you would want to do with this piece of software, guess what, there's a plugin for that. If you so happen not to be able to find one, make your own, put on Github and join the other hundreds (if not thousands) of developers who are constantly building plugins for Laravel. If you want easy image uploading that can be configured properly, get Intervention Image. Want a markdown parser for writing articles or documentation? Use Parsedown. Anything you can think of search for the service first, or be happy with building your own and adding to the list of providers in your   ```config/app.php```.

<img src="http://laracon.us/img/preview.png" class="img-responsive" />

## The Community

The Laravel community is growing more everyday. In fact, according to Google Trends, no other PHP framework is even close to the amount of interest that Laravel receives. I would bet that the way you even seen this article is from a Google search on Laravel. People like me are becoming evangelists of Laravel more and more, but no one is more of an evangelist of Laravel than Jeffery Way, The best way of thinking of Laracasts is, Netflix for Developers.

Paying around $8/month for unlimited high quality videos from someone who is excited to teach and definitely won't put you to sleep is worth so much more. Laracasts comes with three plans, monthly, yearly, and _**FOREVER**_.

The monthly plan as I said before is only $8/month. While yearly is around $90, and for a little under $400 you could get the benefits of Laracasts for life! Laracasts even offers a pass for free to try out the content and see if you like it. Some videos are already free but you'll miss out on all the great content that truly makes it what it is if you go without paying.

### Laracon

Once a year the founder of Laravel, Taylor Otwell, and some of the community's most active developers host a conference also. These conferences are called Laracon, held in the US (United States) and UK (United Kingdom). This year, 2017, it will be held in New York City, NY. Last year it was in Louisville, KY, and they're always looking for more places and people that are willing to host and help.

Laracon provides detailed classes, talks, and networking to get you even further into the Laravel world. Hundreds of developers come together in a serious geekfest to talk about the framework that has helped them out the most. Sadly, I won't be at the coming Laracon, but my team is planning to make our appearance at Laracon US in 2018. I can't wait!

Also, there's *The Laravel Podcast* in which Taylor Otwell and Jeffery Way are frequent guests (actually they're more like co-hosts).

## Conclusion

Laravel is a great tool to write not only functional code but code that is beautifully written and done the right way. Laravel is not only a tool for learning developers but for even the most advanced, it's forgiving and grows with you.

So, What made you choose Laravel? Leave your comments below. Thank you.