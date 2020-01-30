---
layout: page
title: Lectures
permalink: /lectures/
---

# All lectures will be upload here:

* [ Lecture URLs ](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N)

---


# Lectures:


* [ Lecture00-CourseOverview ](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2000-%20Course%20Overview.pdf)

---

* [ Lecture01-TransportLayer(REV) ](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2001-%20Transport%20Layer%20(REV).pdf)

---

* [ Lecture02-(Berkeley)SocketProgramming ](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2002-%20(Berkeley)%20Socket%20Programming.pdf)

---

* [ Lecture03-HTTP 1X ](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2003-%20HTTP%201X.pdf)

---

* [ Lecture04-HTTP 2](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2004-%20HTTP%202.pdf)

---

* [ Lecture05-HTTPS,SSL](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2005-%20HTTPS%2C%20SSL.pdf)

---

* [ Lecture06-XHR](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2006-%20XHR.pdf)

---

* [ Lecture07-SSE](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2007-%20SSE.pdf)

---

* [ Lecture08-WebSocket](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2008-%20WebSocket.pdf)

---

* [ Lecture09-MultimediaStreaming](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2009-%20Multimedia%20Streaming.pdf)

---

* [ Lecture10-WebRTC](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2010-%20WebRTC.pdf)

---

* [ Lecture11-DCN,Data Center Networking(Topologies and Routing)](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2011-%20DCN%2C%20Data%20Center%20Networking%20(Topologies%20and%20Routing).pdf)

---

* [ Lecture12-Part-1](https://drive.iust.ac.ir/index.php/s/YEV4rWxRcKytN4N/download?path=%2F&files=Lecture%2012-PART-1.pdf)

<ul id="archive">
{% for lecture in site.lectures reversed %}
<li class="archiveposturl" style="background: transparent">
<div class="lecture-container">
    {% if lecture.thumbnail %}
    <div class="thumbnail">
      <div class="center-cropped" style="margin-top:5px;margin-bottom:5px;background-image: url('{{ lecture.thumbnail | prepend: site.baseurl }}');">
        <img src="{{ lecture.thumbnail | prepend: site.baseurl }}"/>
      </div>
    </div>
    {% endif %}
    <div class="content">
        <span><a href="
            {% if lecture.slides contains '://' %}
              {{ lecture.slides }} 
            {% else %}
              {{ lecture.slides | prepend: site.baseurl }} 
            {% endif %}">{{ lecture.title }}</a>
        </span><br>

        {% if lecture.tldr %}
            <strong>tl;dr:</strong> 
            {{ lecture.tldr }}
            <br/>
        {% endif %}

        <strong>
            {% include lecture_links.html lecture=lecture %}
        </strong>
    </div>
</div>
</li>
{% endfor %}
</ul>