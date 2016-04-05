---
layout: index
published: true
extra_js:
 - https://learningcircles.p2pu.org/en/studygroups/?course_id=2&callback=renderCircles
---

# Take the course in person

Learning Circles offer the opportunity to work through the course with your local community. Join a Learning Circle near you below, or create your own!

<div id="lc-container" class="row">
<div class="col-md-4">{% include lc-card.html %}</div>
</div>

Or <a href="https://learningcircles.p2pu.org/" class="btn btn-primary">create your own</a>

<script type="text/javascript">
    function renderCircle(circle, template) {
        var html = template.clone();
        html.find('.d-course_title').text(circle.course_title);
        html.find('.d-facilitator').text(circle.facilitator);
        html.find('.d-venue').text(circle.venue);
        html.find('.d-venue_address').text(circle.venue_address);
        html.find('.d-day').text(circle.day + 's');
        html.find('.d-start_date').text(circle.start_date);
        html.find('.d-meeting_time').text(circle.meeting_time); // format time here
        html.find('.d-time_zone').text(circle.time_zone);
        html.find('.d-end_time').text(circle.end_time);
        html.find('.d-weeks').text(circle.weeks);
        html.find('.d-url').attr('href', circle.url);
        if (circle.image_url.length > 0){
            html.find('.d-image_url').attr('src', circle.image_url);
        }
        return html;
    }

    function renderCircles(circles){
        var container = $('#lc-container');
        var template = $(container.children()[0]).clone();
        container.children().remove();
        for (var i = 0; i< circles.length; ++i){
            var lcHtml = renderCircle(circles[i], template);
            container.append(lcHtml);
        }
    }
</script>

# About the course

Educational policy makers have taken note of the phenomenon, and are now investing heavily in projects that attempt to harness this grassroots movement and connect it to STEM and STEAM education, workforce preparedness, and the development of innovative and entrepreneurial skills.

The goal of Making+Learning is to build the capacity of libraries and museums to create and sustain effective makerspaces and related programs for learning within and outside of their own organizations.
