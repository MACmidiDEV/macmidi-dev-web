# MACmidiDEV

## Flask_APP
## run.py = 
##     import os 
##     from flask import Flask, render_template
##     app = Flask(__name__)
##     appRoute will bind indexHTML to "/"
##     @app.route("/")
##     def index():
##         return render_template("index.html")

# route templates
## statement to inject in html
## <li><a href="{{ url_for('ROUTE') }}">CAREERS</a></li>

# inherit templates
## create templates in base.html
##          {% extends 'base.html' %}
#           {% block <VAR> %}    
#               <h1>DIFFcode</h1>
#           {% endblock %}   



{% extends 'base.html' %} {% block content %}
<h2>{{ page_title }}</h2>


{% for member in company %}
<div class="row featurette">
    <div class="col-md-7">
        <h3>{{ member.name }}</h3>
        <p>{{ member.description }}</p>
    </div>
    <div class="col-md-5">
        <img class="featurette-image img-responsive" src="{{ member.image_source }}" alt="Picture of {{ member.name }}">
    </div>
</div>
<hr class="featurette-divider"> {% endfor %} {% endblock %}




  {% for num in list_nums %}
        <p>{{ num }}</p>
    {% endfor %}


<img src="{{ url_for('static', filename='img/kawhi.jpg') }}"></img>

{% extends 'base.html' %} 
{% block content %}
    <h2>{{ page_title }}</h2>

  <hr class = "featurette-divider">
{% for champ in champs %}
    <div class="row featurette">
        <div class="col-md-5">
            <h4>{{ champ.year }}</h4>
            <h6>NBA CHAMPIONS</h6>
            <h5>{{ champ.team }}</h5>
            <h3>MVP</h3>
            <h2>{{ champ.mvp }}</h2>
        </div>
        <div class="col-md-7">
<img class="featurette-image img-responsive" src="{{ champ.logo }}" alt="{{ champ.year }}ChampLogo">
                  
        </div>
        
    </div>
<hr class = "featurette-divider">

</div>
{% endblock %}