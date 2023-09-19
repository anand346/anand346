```php
<?php

namespace AnandRaj;

class About extends Me
{
    public function getBasicDetails(): array
    {
        return [
            'details' => [
                'name'     => 'Anand Raj',
                'mail'     => 'rajanand9039@gmail.com',
                'resume'   => 'https://drive.google.com/file/d/13ml4INw8jQldEmnKIZqI8f2yaa_mL_55/view',
                'linkedin' => 'https://linkedin.com/in/anand346',
                'blogs'    => 'https://bepractical.tech/blogs',
            ]
        ];
    }

    public function getKnowledgeBase(): array
    {
        return [
            Php::class,
            Javascript::class,
            CodeIgniter::class,
            ReactJs::class,
            NextJs::class,
            TailwindCss::class,
        ];
    }

    public function getGoal(): string
    {
        return 'To contribute to open source.';
    }
}
```
![Snake animation](https://github.com/thepiyushmalhotra/thepiyushmalhotra/blob/output/github-contribution-grid-snake.svg)
