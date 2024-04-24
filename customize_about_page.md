---
layout: default
title: Customize about page
parent: Customizing a Minima Jekyll theme
nav_order: 16
---

To customize the default about page "about.markdown" in the Minima theme, follow these steps:

1. **In the "_layouts" Folder, we will create a new layout file named "about.html".**

    An Example of custom "about.html" layout page.

    ```ts
    {% raw %}
    ---
    layout: default
    ---
    <div class="post-content">
        {{ content }}
    </div>
    {% endraw %}
    ```
2. **Locate the "about.markdown" file in your Jekyll project, and open it.**
3. **In your about.markdown file, update front matter to specify your page layout.**

    For Example:

    ```ts
    ---
    layout: about
    ---
    ```
4. **Add your about page custom content.**

- Below we will provide you with an example of an about page that contains an Info section, a Vision section, a Video section, and a teams section.

    **Example of about.markdown page:**

        ```ts
        ---
        layout: about
        permalink: /about-us/
        ---

        <div class="aboutus">

        <div class="about-us blue-background">
            <div class="page-wrapper">
                <div class="title"><h2>About Us</h2></div>
                <div class="about-us-content">
                    <p>
                        Sed sodales magna et nisl accumsan ornare. Etiam sed eros arcu. Donec turpis tellus, congue id ipsum eu, egestas viverra dui. Cras tincidunt, felis a interdum aliquet, felis erat porta arcu, vitae scelerisque ex mi a diam. Etiam consequat ullamcorper elit ut dignissim. Vestibulum venenatis, leo eget luctus feugiat, turpis lacus sollicitudin velit, id malesuada lectus orci vel tortor. Ut blandit magna blandit turpis mattis ultrices.
                    </p>
                </div>  
            </div>
        </div>

        <div class="about-us-vision">
            <div class="page-wrapper">
                <div class="about-us-vision-content">
                    <div class="about-us-vision-image">
                        <img src="/assets/img/about_vision_image.jpg" alt="">
                        <p>Image retrived from https://pixabay.com/</p>
                    </div>
                    <div class="about-us-vision-text">    
                        <p>    
                        Donec justo quam, hendrerit eget elementum quis, dignissim vel neque. Nullam nunc magna, aliquet non lacinia sit amet, placerat dapibus erat. Duis sodales porta nunc, hendrerit blandit velit sagittis sit amet. Ut in est nisi. In ut hendrerit nulla. Duis quis purus libero. Ut vulputate pellentesque ex a egestas. Ut est felis, pulvinar quis tincidunt a, gravida in mauris. Cras id velit at felis dictum dictum. Sed efficitur nisi et nunc pharetra, id maximus dolor hendrerit. Praesent finibus placerat neque, sed accumsan nisl pulvinar eu.
                        </p>
                        <p>
                        Praesent at ultricies justo. Mauris mollis sit amet magna sit amet commodo. Cras at mattis quam. Donec vel tristique nibh, et bibendum quam. Aliquam tempor nunc ac sapien finibus malesuada. Duis viverra luctus metus, vitae malesuada metus elementum at. Vestibulum vulputate, quam eget mattis blandit, tortor metus rhoncus felis, a tincidunt arcu lectus nec magna. Praesent vel ex in mauris varius tincidunt. Aliquam rhoncus lectus in ipsum pretium condimentum. Sed suscipit egestas tempor. Vivamus nisl velit, aliquam a vestibulum eget, accumsan sed lacus. Praesent luctus ornare sollicitudin.
                        </p>
                    </div>
                </div>
            </div>
        </div>

        <div class="about-us-video">
            <div class="page-wrapper video-content">
                <div class="video">
                    <iframe width="724" height="407" src="https://cdn.pixabay.com/video/2015/09/27/846-140823862_large.mp4" title="Chandrima Chakraborty | 2019 College of New Scholars | McMaster University" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                </div>
                <div class="about-us-video-content">
                    <p>Curabitur neque augue, vestibulum consectetur iaculis ac, interdum eget nulla.<br />
                    PUBLISHED DATE: April 23<br /></p>
                    <a href="">Find out more</a>
                </div>
            </div>
        </div>

        <div class="about-us-team yellow-background">
            <div class="page-wrapper">
                <div class="title"><h2>TEAM Members</h2></div>
                    <div class="about-us-teams">
                        <div class="about-us-team-member">
                            <div class="about-us-team-member-image">
                                <img src="/assets/img/about_teams.webp" alt="" />
                            </div>
                            <div class="about-us-team-member-name">
                                <p>Name</p>
                            </div>
                            <div class="line"></div>
                            <div class="about-us-team-member-position">
                                <p>Job Title</p>
                            </div>
                            <div class="about-us-team-member-department">
                                <p>Department</p>
                            </div>
                        </div>
                        <div class="about-us-team-member">
                            <div class="about-us-team-member-image">
                                <img src="/assets/img/about_teams.webp" alt="" />
                            </div>
                            <div class="about-us-team-member-name">
                                <p>Name</p>
                            </div>
                            <div class="line"></div>
                            <div class="about-us-team-member-position">
                                <p>Job Title</p>
                            </div>
                            <div class="about-us-team-member-department">
                                <p>Department</p>
                            </div>
                        </div>
                        <div class="about-us-team-member">
                            <div class="about-us-team-member-image">
                                <img src="/assets/img/about_teams.webp" alt="" />
                            </div>
                            <div class="about-us-team-member-name">
                                <p>Name</p>
                            </div>
                            <div class="line"></div>
                            <div class="about-us-team-member-position">
                                <p>Job Title</p>
                            </div>
                            <div class="about-us-team-member-department">
                                <p>Department</p>
                            </div>
                        </div>
                        <div class="about-us-team-member">
                            <div class="about-us-team-member-image">
                                <img src="/assets/img/about_teams.webp" alt="" />
                            </div>
                            <div class="about-us-team-member-name">
                                <p>Name</p>
                            </div>
                            <div class="line"></div>
                            <div class="about-us-team-member-position">
                                <p>Job Title</p>
                            </div>
                            <div class="about-us-team-member-department">
                                <p>Department</p>
                            </div>
                        </div>
                        <div class="about-us-team-member">
                            <div class="about-us-team-member-image">
                                <img src="/assets/img/about_teams.webp" alt="" />
                            </div>
                            <div class="about-us-team-member-name">
                                <p>Name</p>
                            </div>
                            <div class="line"></div>
                            <div class="about-us-team-member-position">
                                <p>Job Title</p>
                            </div>
                            <div class="about-us-team-member-department">
                                <p>Department</p>
                            </div>
                        </div>
                        <div class="about-us-team-member">
                            <div class="about-us-team-member-image">
                                <img src="/assets/img/about_teams.webp" alt="" />
                            </div>
                            <div class="about-us-team-member-name">
                                <p>Name</p>
                            </div>
                            <div class="line"></div>
                            <div class="about-us-team-member-position">
                                <p>Job Title</p>
                            </div>
                            <div class="about-us-team-member-department">
                                <p>Department</p>
                            </div>
                        </div>
                        <div class="about-us-team-member">
                            <div class="about-us-team-member-image">
                                <img src="/assets/img/about_teams.webp" alt="" />
                            </div>
                            <div class="about-us-team-member-name">
                                <p>Name</p>
                            </div>
                            <div class="line"></div>
                            <div class="about-us-team-member-position">
                                <p>Job Title</p>
                            </div>
                            <div class="about-us-team-member-department">
                                <p>Department</p>
                            </div>
                        </div>
                        <div class="about-us-team-member">
                            <div class="about-us-team-member-image">
                                <img src="/assets/img/about_teams.webp" alt="" />
                            </div>
                            <div class="about-us-team-member-name">
                                <p>Name</p>
                            </div>
                            <div class="line"></div>
                            <div class="about-us-team-member-position">
                                <p>Job Title</p>
                            </div>
                            <div class="about-us-team-member-department">
                                <p>Department</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        ```

- Below is the custom stylesheet for the about.markdown page to be added in the custom.scss file.

    **Example of Custom stylesheet for the about.md page**

        ```ts
        //custom stylesheet for the About page
        .about-us-content {
            padding: 0 0 16px 45px;
            border-bottom: 2px solid white;
        }
        .title h2 {
            font-weight: bold;
        }
        .about-us-vision-content {
            display: flex;
            align-items: center;
            column-gap: 56px;
        }
        .about-us-vision-image {
            flex: 1;
            font-size: 10px;
        }
        .about-us-vision-text {
            flex: 1;
        }
        .video-content {
            display: flex;
            align-items: center;
            column-gap: 50px;
        }
        .about-us-video-content {
            text-align: center;
            font-weight: bold;
        }
        .about-us-video-content p {
            margin-bottom: 35px;
        }
        .about-us-video-content a {
            background: #5d6247;
            color: white;
            padding: 15px 36px;
            border-radius: 50px;
        }
        .about-us-teams {
            display: flex;
            flex-wrap: wrap;
            column-gap: 10px;
            row-gap: 29px;
            justify-content: space-between;
        }

        .about-us-team-member {
            flex: 0 0 23%;
            background: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 35px 40px;
            row-gap: 12px;
        }
        .about-us-team-member img {
            border-radius: 50%;
            border: 3px solid #fdbf57;
        }
        .about-us-team-member .line {
            margin: 0 auto;
        }
        .about-us-team-member .line {
            width: 49px;
            border-bottom: 5px solid #b6b333;
        }
        ```