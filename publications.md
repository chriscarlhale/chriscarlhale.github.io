---
layout: page
title: Publications
permalink: /publications
pubs: 
  - name: Academic Culture as Content
    publisher: Springer
    date: 2020/12
    title: Self-Assessment in the CLIL Classroom in the International Liberal Arts University
    author:
      - name: Chris Carl Hale
      - name: Alexander Nanni    
    desc: Joint Editing and Writing, Foreign language education, Education, Education on school subjects and activities, English
    image: /assets/images/assessment_and_learning_in_content_and_language_integrated_learning_clil_classrooms_approaches_and_conceptualisations.jpg
    urls:
      - site: Amazon       
        href: https://www.amazon.co.jp/-/en/Mark-deBoer/dp/3030541274/ref=tmm_hrd_title_0?_encoding=UTF8&qid=1605769044&sr=8-1
      - site: Springer
        href: https://link.springer.com/book/10.1007%2F978-3-030-54128-6#about

  - name: An in-service TESOL practicum in Japan
    publisher: Springer    
    date: 2020/11
    title: 
    author:
      - name: Bill Snyder
      - name: Chris Carl Hale
      - name: Gordon Myskow
    desc: Joint Editing and Writing, Foreign language education, Education, Education on school subjects and activities, English
    image: /assets/images/current_prospectives_on_the_tesol_practicum_cases_from_around_the_world.jpg
    urls:
      - site: Amazon       
        href: https://www.amazon.co.jp/-/en/Andrzej-Cirocki-ebook/dp/B084F83ZLD/ref=sr_1_1?dchild=1&keywords=Current+Perspectives+on+the+TESOL+Practicum&qid=1609823882&sr=8-1
      - site: Springer
        href: https://link.springer.com/book/10.1007%2F978-3-030-28756-6

  - name: Teaching English at Japanese Universities
    publisher: Routledge
    date: 2018/11    
    title: A new Handbook
    author:
      - name: Paul Wadden
      - name: Chris Carl Hale
    desc: Scholarly Book, Joint Editing and Writing, Foreign language education, Education, Sociology of education, English
    image: /assets/images/teaching_english_at_japanese_universities_a_new_handbook.jpg
    urls:
      - site: Amazon       
        href: https://www.amazon.co.jp/dp/1138550396/?coliid=IGO4902J906QC&colid=TLGWXFAEBJFH&psc=0&ref_=lv_ov_lig_dp_it
      - site: Routledge
        href: https://www.routledge.com/Teaching-English-at-Japanese-Universities-A-New-Handbook/Wadden-Hale/p/book/9781138550391
      - site: ASIN
        href: http://amazon.co.jp/o/ASIN/1138550396

  - name: Real world listening in the Japanese university classroom (Chapter in edited volume)
    publisher: Routledge
    date: 2018/11
    title: 
    author: 
      - name: Chris Carl Hale
    desc: Single Author, Foreign language education, Education, Sociology of education, English
    image: /assets/images/teaching_english_at_japanese_universities_a_new_handbook.jpg
    urls:
      - site: Amazon       
        href: https://www.amazon.co.jp/dp/1138550396/?coliid=IGO4902J906QC&colid=TLGWXFAEBJFH&psc=0&ref_=lv_ov_lig_dp_it
      
  - name: "The landscape of Japanese higher education: An introduction (Chapter in edited volume)"
    publisher: Routledge
    date: 2018/11
    title: 
    author: 
      - name: Chris Carl Hale
      - name: Paul Wadden
    desc: Joint Editing and Writing, Foreign language education, Education, Sociology of education, English
    image: /assets/images/teaching_english_at_japanese_universities_a_new_handbook.jpg 
    urls:
      - site: Amazon       
        href: https://www.amazon.co.jp/dp/1138550396/?coliid=IGO4902J906QC&colid=TLGWXFAEBJFH&psc=0&ref_=lv_ov_lig_dp_it

  - name: Types of universities in Japan (Chapter in edited volume)
    publisher: Routledge
    date: 2018/11
    title: 
    author:
      - name: Chris Carl Hale
      - name: Paul Wadden
    desc: Joint Editing and Writing, Foreign language education, Education, Sociology of education, English
    image: /assets/images/teaching_english_at_japanese_universities_a_new_handbook.jpg
    urls:
      - site: Amazon       
        href: https://www.amazon.co.jp/dp/1138550396/?coliid=IGO4902J906QC&colid=TLGWXFAEBJFH&psc=0&ref_=lv_ov_lig_dp_it
      - site:

  - name: "Negotiating the effects of transnational education: The experience of graduate students in an American teacher-education program"
    publisher: Japan ProQuest LLC
    date: 2015/03
    title:
    author: 
      - name: Chris Carl Hale
    desc: Scholarly Book, Single Author, Foreign language education, Education, English
    image: /assets/images/negotiating_the_effects_of_transnational_education.png

  - name: "Charting new courses: Second language action research in Japanese junior and senior high schools"
    publisher: Accents Asia Press
    date: 2008/04
    title: 
    author: 
      - name: Chris Carl Hale
      - name: Janell Pekkain
      - name: Kristen Carlson
    desc: Scholarly Book, Multiple Authorship , Education on school subjects and activities, Foreign language education, English
    image: /assets/images/charting_new_courses_second_language_action_research_in_japanese_junior_and_senior_high_schools_accents_asia_the_journal_for_second_language_education_in_east_asia.jpg

---
{% for pub in page.pubs %}
  <div class="card m-2 p-2" style="">    
    <div class="row">        
      <div class="col">        
        <div class="card-body">
          <div class="card-text"><small class="text-muted">{{ pub.publisher }} {{ pub.date }}</small></div>
          <h4 class="card-title">{{ pub.name.title }}</h4>
          <h5 class="card-title">{{ pub.name }}</h5>
          <p class="card-text">{{ pub.desc }}</p>
          <p class="card-text">By: 
            {% for auth in pub.author %}
              {{ auth.name }}{% if forloop.last %}{% else %}, {% endif %}
            {% endfor %}    
          </p>
          {% for url in pub.urls %}
            <a href="{{ url.site.href }}" target="_blank" class="btn btn-primary">{{ url.site }}</a>
          {% endfor %}    
        </div>
      </div>      
      {% if pub.image %}
      <div class="col-md-2">
        <img src="{{ pub.image }}" class="pub-image float-end" alt="{{ pub.name }}">
      </div>
      {% endif %}
    </div>
  </div>
{% endfor %}


