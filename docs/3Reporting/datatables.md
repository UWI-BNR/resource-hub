<style>
  /* Wrapper: allows vertical scroll while header stays visible */
  .bnr-table-wrapper {
    max-height: 500px;
    overflow-y: auto;
    margin: 1rem 0;
  }

  .bnr-table {
    width: 100%;
    border-collapse: collapse;
  }

  .bnr-table th,
  .bnr-table td {
    padding: 0.35rem 0.5rem;
    border: none;
    border-bottom: 1px solid #dddddd;
    text-align: left;
    white-space: nowrap;
  }

  .bnr-table th:first-child,
  .bnr-table td:first-child {
    text-align: left;
  }

  .bnr-table tbody tr:nth-child(even) {
    background-color: rgba(0, 0, 0, 0.03);
  }

  .bnr-table thead th {
    position: sticky;
    top: 0;
    z-index: 2;
    background-color: var(--md-surface, #ffffff);
  }

  .bnr-table thead tr:last-child th {
    border-bottom: 2px solid #cccccc;
  }

  @media (prefers-color-scheme: dark) {
    .bnr-table tbody tr:nth-child(even) {
      background-color: rgba(255, 255, 255, 0.04);
    }
  }

  .bnr-year-block {
    margin: 1rem 0 1.5rem 0;
  }

  .bnr-year-label {
    font-weight: 600;
    margin-right: 0.5rem;
  }

  .bnr-year-select {
    padding: 0.2rem 0.4rem;
    font-size: 0.9rem;
  }

/* Show 2023 table by default (while keeping other years hidden) */
.bnr-year-table {
  display: none;
}
.bnr-year-table[data-bnr-year="2023"] {
  display: block;
}

</style>


# BNR Data Tables 2023

## Introduction
This page provides the full set of technical tabulations generated to support our 2023 BNR cardiovascular disease briefings. These tables present the underlying weekly, annual, and stratified counts for stroke, acute myocardial infarction (AMI), and all-CVD events, offering a transparent view of the data used in each analysis. They serve as the authoritative reference for all figures and metrics reported in each of our BNR briefings, ensuring reproducibility, comparability across years, and clarity for users who wish to explore the detailed numbers behind the summaries.

???- info "Data Confidentiality Note"

    The tables on this page present a range of population-level health statistics — for example, weekly counts, annual totals, incidence rates, percentages, averages, and other summary measures. These tables describe overall patterns in the population, not information about any specific person.

    All data shown here are fully anonymised:

    - no table includes personal details such as age, sex, address, or any other characteristic that could identify someone
    - the values represent combined summaries, never individual records
    - even when numbers are small, they cannot be linked back to any individual
    - no one can “reverse engineer” these summaries to work out who experienced a particular health event

    Because the information is strictly aggregate and non-identifiable, it meets the requirements of both the Barbados Data Protection Act and GDPR for the release of anonymised data. It is therefore safe and appropriate to share these statistics publicly.

## **Table 1.** Annual Event Count by Year 
### Presenting Stroke and Heart Attack Events by Year for Women and Men
<div class="bnr-table-wrapper">
  <table class="bnr-table">
    <thead>
      <tr>
        <th></th>
        <th colspan="9">CVD Event Type</th>
      </tr>
      <tr>
        <th rowspan="3">CVD event year</th>
        <th colspan="3">Stroke</th>
        <th colspan="3">AMI</th>
        <th colspan="3">Total</th>
      </tr>
      <tr>
        <th colspan="3">Patient sex</th>
        <th colspan="3">Patient sex</th>
        <th colspan="3">Patient sex</th>
      </tr>
      <tr>
        <th>Female</th>
        <th>Male</th>
        <th>Total</th>
        <th>Female</th>
        <th>Male</th>
        <th>Total</th>
        <th>Female</th>
        <th>Male</th>
        <th>Total</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>2009</td><td>315</td><td>234</td><td>549</td><td>82</td><td>101</td><td>183</td><td>397</td><td>335</td><td>732</td></tr>
      <tr><td>2010</td><td>321</td><td>260</td><td>581</td><td>179</td><td>165</td><td>344</td><td>500</td><td>425</td><td>925</td></tr>
      <tr><td>2011</td><td>302</td><td>261</td><td>563</td><td>126</td><td>168</td><td>294</td><td>428</td><td>429</td><td>857</td></tr>
      <tr><td>2012</td><td>321</td><td>257</td><td>578</td><td>201</td><td>203</td><td>404</td><td>522</td><td>460</td><td>982</td></tr>
      <tr><td>2013</td><td>367</td><td>327</td><td>694</td><td>161</td><td>191</td><td>352</td><td>528</td><td>518</td><td>1,046</td></tr>
      <tr><td>2014</td><td>316</td><td>268</td><td>584</td><td>190</td><td>220</td><td>410</td><td>506</td><td>488</td><td>994</td></tr>
      <tr><td>2015</td><td>319</td><td>267</td><td>586</td><td>157</td><td>169</td><td>326</td><td>476</td><td>436</td><td>912</td></tr>
      <tr><td>2016</td><td>393</td><td>330</td><td>723</td><td>189</td><td>250</td><td>439</td><td>582</td><td>580</td><td>1,162</td></tr>
      <tr><td>2017</td><td>348</td><td>302</td><td>650</td><td>214</td><td>253</td><td>467</td><td>562</td><td>555</td><td>1,117</td></tr>
      <tr><td>2018</td><td>355</td><td>327</td><td>682</td><td>214</td><td>269</td><td>483</td><td>569</td><td>596</td><td>1,165</td></tr>
      <tr><td>2019</td><td>396</td><td>362</td><td>758</td><td>276</td><td>271</td><td>547</td><td>672</td><td>633</td><td>1,305</td></tr>
      <tr><td>2020</td><td>364</td><td>335</td><td>699</td><td>262</td><td>285</td><td>547</td><td>626</td><td>620</td><td>1,246</td></tr>
      <tr><td>2021</td><td>357</td><td>334</td><td>691</td><td>222</td><td>245</td><td>467</td><td>579</td><td>579</td><td>1,158</td></tr>
      <tr><td>2022</td><td>384</td><td>384</td><td>768</td><td>257</td><td>313</td><td>570</td><td>641</td><td>697</td><td>1,338</td></tr>
      <tr><td>2023</td><td>407</td><td>396</td><td>803</td><td>267</td><td>297</td><td>564</td><td>674</td><td>693</td><td>1,367</td></tr>
      <tr>
        <td><strong>Total</strong></td>
        <td><strong>5,265</strong></td>
        <td><strong>4,644</strong></td>
        <td><strong>9,909</strong></td>
        <td><strong>2,997</strong></td>
        <td><strong>3,400</strong></td>
        <td><strong>6,397</strong></td>
        <td><strong>8,262</strong></td>
        <td><strong>8,044</strong></td>
        <td><strong>16,306</strong></td>
      </tr>
    </tbody>
  </table>
</div>

[Download Data](../downloads/data/bnr-cvd-2023-table1.xlsx){ .md-button .btn-right}
<br/><br/>

---

## **Table 2.** Weekly Event Count by Year 
### Presenting Stroke and Heart Attack Events by Week for Women and Men


<div class="bnr-year-block">
  <label class="bnr-year-label">Select year:</label>
  <select class="bnr-year-select">
    <option value="2010">2010</option>
    <option value="2011">2011</option>
    <option value="2012">2012</option>
    <option value="2013">2013</option>
    <option value="2014">2014</option>
    <option value="2015">2015</option>
    <option value="2016">2016</option>
    <option value="2017">2017</option>
    <option value="2018">2018</option>
    <option value="2019">2019</option>
    <option value="2020">2020</option>
    <option value="2021">2021</option>
    <option value="2022">2022</option>
    <option value="2023" selected>2023</option>
  </select>

<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2010">
  <table class="bnr-table">
    <thead>
      <tr>
        <th>Week of event (woe)</th>
        <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
      </tr>
      <tr>
        <th></th>
        <th>Stroke</th>
        <th>AMI</th>
        <th>Total</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>1</td><td>10</td><td>8</td><td>18</td></tr>
      <tr><td>2</td><td>18</td><td>8</td><td>26</td></tr>
      <tr><td>3</td><td>13</td><td>7</td><td>20</td></tr>
      <tr><td>4</td><td>7</td><td>8</td><td>15</td></tr>
      <tr><td>5</td><td>16</td><td>11</td><td>27</td></tr>
      <tr><td>6</td><td>14</td><td>2</td><td>16</td></tr>
      <tr><td>7</td><td>13</td><td>6</td><td>19</td></tr>
      <tr><td>8</td><td>10</td><td>6</td><td>16</td></tr>
      <tr><td>9</td><td>15</td><td>4</td><td>19</td></tr>
      <tr><td>10</td><td>13</td><td>7</td><td>20</td></tr>
      <tr><td>11</td><td>11</td><td>3</td><td>14</td></tr>
      <tr><td>12</td><td>11</td><td>7</td><td>18</td></tr>
      <tr><td>13</td><td>10</td><td>6</td><td>16</td></tr>
      <tr><td>14</td><td>5</td><td>7</td><td>12</td></tr>
      <tr><td>15</td><td>3</td><td>10</td><td>13</td></tr>
      <tr><td>16</td><td>10</td><td>3</td><td>13</td></tr>
      <tr><td>17</td><td>12</td><td>8</td><td>20</td></tr>
      <tr><td>18</td><td>13</td><td>6</td><td>19</td></tr>
      <tr><td>19</td><td>9</td><td>5</td><td>14</td></tr>
      <tr><td>20</td><td>16</td><td>6</td><td>22</td></tr>
      <tr><td>21</td><td>15</td><td>6</td><td>21</td></tr>
      <tr><td>22</td><td>10</td><td>4</td><td>14</td></tr>
      <tr><td>23</td><td>13</td><td>7</td><td>20</td></tr>
      <tr><td>24</td><td>8</td><td>6</td><td>14</td></tr>
      <tr><td>25</td><td>8</td><td>4</td><td>12</td></tr>
      <tr><td>26</td><td>9</td><td>3</td><td>12</td></tr>
      <tr><td>27</td><td>7</td><td>5</td><td>12</td></tr>
      <tr><td>28</td><td>11</td><td>10</td><td>21</td></tr>
      <tr><td>29</td><td>11</td><td>7</td><td>18</td></tr>
      <tr><td>30</td><td>10</td><td>2</td><td>12</td></tr>
      <tr><td>31</td><td>8</td><td>9</td><td>17</td></tr>
      <tr><td>32</td><td>15</td><td>5</td><td>20</td></tr>
      <tr><td>33</td><td>11</td><td>5</td><td>16</td></tr>
      <tr><td>34</td><td>12</td><td>2</td><td>14</td></tr>
      <tr><td>35</td><td>11</td><td>10</td><td>21</td></tr>
      <tr><td>36</td><td>12</td><td>7</td><td>19</td></tr>
      <tr><td>37</td><td>10</td><td>7</td><td>17</td></tr>
      <tr><td>38</td><td>10</td><td>9</td><td>19</td></tr>
      <tr><td>39</td><td>13</td><td>9</td><td>22</td></tr>
      <tr><td>40</td><td>14</td><td>9</td><td>23</td></tr>
      <tr><td>41</td><td>8</td><td>8</td><td>16</td></tr>
      <tr><td>42</td><td>10</td><td>4</td><td>14</td></tr>
      <tr><td>43</td><td>9</td><td>2</td><td>11</td></tr>
      <tr><td>44</td><td>10</td><td>10</td><td>20</td></tr>
      <tr><td>45</td><td>14</td><td>11</td><td>25</td></tr>
      <tr><td>46</td><td>8</td><td>9</td><td>17</td></tr>
      <tr><td>47</td><td>10</td><td>9</td><td>19</td></tr>
      <tr><td>48</td><td>9</td><td>7</td><td>16</td></tr>
      <tr><td>49</td><td>9</td><td>5</td><td>14</td></tr>
      <tr><td>50</td><td>13</td><td>2</td><td>15</td></tr>
      <tr><td>51</td><td>19</td><td>8</td><td>27</td></tr>
      <tr><td>52</td><td>15</td><td>15</td><td>30</td></tr>
      <tr><td>Total</td><td>581</td><td>344</td><td>925</td></tr>
    </tbody>
  </table>
</div>

<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2011">
  <table class="bnr-table">
    <thead>
      <tr>
        <th>Week of event (woe)</th>
        <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
      </tr>
      <tr>
        <th></th>
        <th>Stroke</th>
        <th>AMI</th>
        <th>Total</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>1</td><td>8</td><td>5</td><td>13</td></tr>
      <tr><td>2</td><td>4</td><td>2</td><td>6</td></tr>
      <tr><td>3</td><td>3</td><td>7</td><td>10</td></tr>
      <tr><td>4</td><td>18</td><td>5</td><td>23</td></tr>
      <tr><td>5</td><td>15</td><td>9</td><td>24</td></tr>
      <tr><td>6</td><td>11</td><td>2</td><td>13</td></tr>
      <tr><td>7</td><td>10</td><td>2</td><td>12</td></tr>
      <tr><td>8</td><td>11</td><td>7</td><td>18</td></tr>
      <tr><td>9</td><td>12</td><td>2</td><td>14</td></tr>
      <tr><td>10</td><td>8</td><td>7</td><td>15</td></tr>
      <tr><td>11</td><td>13</td><td>8</td><td>21</td></tr>
      <tr><td>12</td><td>15</td><td>3</td><td>18</td></tr>
      <tr><td>13</td><td>11</td><td>5</td><td>16</td></tr>
      <tr><td>14</td><td>14</td><td>7</td><td>21</td></tr>
      <tr><td>15</td><td>15</td><td>2</td><td>17</td></tr>
      <tr><td>16</td><td>11</td><td>5</td><td>16</td></tr>
      <tr><td>17</td><td>12</td><td>7</td><td>19</td></tr>
      <tr><td>18</td><td>12</td><td>8</td><td>20</td></tr>
      <tr><td>19</td><td>9</td><td>5</td><td>14</td></tr>
      <tr><td>20</td><td>14</td><td>12</td><td>26</td></tr>
      <tr><td>21</td><td>8</td><td>12</td><td>20</td></tr>
      <tr><td>22</td><td>8</td><td>5</td><td>13</td></tr>
      <tr><td>23</td><td>7</td><td>2</td><td>9</td></tr>
      <tr><td>24</td><td>6</td><td>5</td><td>11</td></tr>
      <tr><td>25</td><td>9</td><td>8</td><td>17</td></tr>
      <tr><td>26</td><td>8</td><td>3</td><td>11</td></tr>
      <tr><td>27</td><td>10</td><td>5</td><td>15</td></tr>
      <tr><td>28</td><td>18</td><td>8</td><td>26</td></tr>
      <tr><td>29</td><td>11</td><td>9</td><td>20</td></tr>
      <tr><td>30</td><td>5</td><td>3</td><td>8</td></tr>
      <tr><td>31</td><td>11</td><td>7</td><td>18</td></tr>
      <tr><td>32</td><td>11</td><td>6</td><td>17</td></tr>
      <tr><td>33</td><td>8</td><td>8</td><td>16</td></tr>
      <tr><td>34</td><td>10</td><td>6</td><td>16</td></tr>
      <tr><td>35</td><td>12</td><td>7</td><td>19</td></tr>
      <tr><td>36</td><td>15</td><td>6</td><td>21</td></tr>
      <tr><td>37</td><td>9</td><td>3</td><td>12</td></tr>
      <tr><td>38</td><td>10</td><td>5</td><td>15</td></tr>
      <tr><td>39</td><td>14</td><td>2</td><td>16</td></tr>
      <tr><td>40</td><td>17</td><td>7</td><td>24</td></tr>
      <tr><td>41</td><td>12</td><td>4</td><td>16</td></tr>
      <tr><td>42</td><td>14</td><td>7</td><td>21</td></tr>
      <tr><td>43</td><td>10</td><td>5</td><td>15</td></tr>
      <tr><td>44</td><td>12</td><td>5</td><td>17</td></tr>
      <tr><td>45</td><td>9</td><td>5</td><td>14</td></tr>
      <tr><td>46</td><td>11</td><td>8</td><td>19</td></tr>
      <tr><td>47</td><td>8</td><td>2</td><td>10</td></tr>
      <tr><td>48</td><td>14</td><td>5</td><td>19</td></tr>
      <tr><td>49</td><td>9</td><td>5</td><td>14</td></tr>
      <tr><td>50</td><td>6</td><td>6</td><td>12</td></tr>
      <tr><td>51</td><td>15</td><td>3</td><td>18</td></tr>
      <tr><td>52</td><td>10</td><td>12</td><td>22</td></tr>
      <tr><td>Total</td><td>563</td><td>294</td><td>857</td></tr>
    </tbody>
  </table>
</div>

<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2012">
  <table class="bnr-table">
    <thead>
      <tr>
        <th>Week of event (woe)</th>
        <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
      </tr>
      <tr>
        <th></th>
        <th>Stroke</th>
        <th>AMI</th>
        <th>Total</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>1</td><td>11</td><td>9</td><td>20</td></tr>
      <tr><td>2</td><td>16</td><td>9</td><td>25</td></tr>
      <tr><td>3</td><td>11</td><td>8</td><td>19</td></tr>
      <tr><td>4</td><td>10</td><td>8</td><td>18</td></tr>
      <tr><td>5</td><td>11</td><td>7</td><td>18</td></tr>
      <tr><td>6</td><td>10</td><td>7</td><td>17</td></tr>
      <tr><td>7</td><td>4</td><td>9</td><td>13</td></tr>
      <tr><td>8</td><td>15</td><td>9</td><td>24</td></tr>
      <tr><td>9</td><td>13</td><td>7</td><td>20</td></tr>
      <tr><td>10</td><td>9</td><td>6</td><td>15</td></tr>
      <tr><td>11</td><td>6</td><td>9</td><td>15</td></tr>
      <tr><td>12</td><td>12</td><td>6</td><td>18</td></tr>
      <tr><td>13</td><td>12</td><td>6</td><td>18</td></tr>
      <tr><td>14</td><td>7</td><td>15</td><td>22</td></tr>
      <tr><td>15</td><td>12</td><td>6</td><td>18</td></tr>
      <tr><td>16</td><td>10</td><td>5</td><td>15</td></tr>
      <tr><td>17</td><td>18</td><td>11</td><td>29</td></tr>
      <tr><td>18</td><td>11</td><td>8</td><td>19</td></tr>
      <tr><td>19</td><td>15</td><td>7</td><td>22</td></tr>
      <tr><td>20</td><td>16</td><td>10</td><td>26</td></tr>
      <tr><td>21</td><td>11</td><td>8</td><td>19</td></tr>
      <tr><td>22</td><td>11</td><td>9</td><td>20</td></tr>
      <tr><td>23</td><td>10</td><td>6</td><td>16</td></tr>
      <tr><td>24</td><td>20</td><td>4</td><td>24</td></tr>
      <tr><td>25</td><td>9</td><td>2</td><td>11</td></tr>
      <tr><td>26</td><td>17</td><td>6</td><td>23</td></tr>
      <tr><td>27</td><td>20</td><td>8</td><td>28</td></tr>
      <tr><td>28</td><td>5</td><td>4</td><td>9</td></tr>
      <tr><td>29</td><td>8</td><td>11</td><td>19</td></tr>
      <tr><td>30</td><td>10</td><td>6</td><td>16</td></tr>
      <tr><td>31</td><td>9</td><td>3</td><td>12</td></tr>
      <tr><td>32</td><td>16</td><td>12</td><td>28</td></tr>
      <tr><td>33</td><td>10</td><td>10</td><td>20</td></tr>
      <tr><td>34</td><td>16</td><td>10</td><td>26</td></tr>
      <tr><td>35</td><td>17</td><td>4</td><td>21</td></tr>
      <tr><td>36</td><td>9</td><td>9</td><td>18</td></tr>
      <tr><td>37</td><td>9</td><td>7</td><td>16</td></tr>
      <tr><td>38</td><td>7</td><td>8</td><td>15</td></tr>
      <tr><td>39</td><td>13</td><td>9</td><td>22</td></tr>
      <tr><td>40</td><td>12</td><td>6</td><td>18</td></tr>
      <tr><td>41</td><td>10</td><td>8</td><td>18</td></tr>
      <tr><td>42</td><td>10</td><td>9</td><td>19</td></tr>
      <tr><td>43</td><td>14</td><td>6</td><td>20</td></tr>
      <tr><td>44</td><td>7</td><td>7</td><td>14</td></tr>
      <tr><td>45</td><td>9</td><td>7</td><td>16</td></tr>
      <tr><td>46</td><td>5</td><td>6</td><td>11</td></tr>
      <tr><td>47</td><td>5</td><td>10</td><td>15</td></tr>
      <tr><td>48</td><td>11</td><td>4</td><td>15</td></tr>
      <tr><td>49</td><td>4</td><td>9</td><td>13</td></tr>
      <tr><td>50</td><td>7</td><td>11</td><td>18</td></tr>
      <tr><td>51</td><td>14</td><td>12</td><td>26</td></tr>
      <tr><td>52</td><td>14</td><td>11</td><td>25</td></tr>
      <tr><td>Total</td><td>578</td><td>404</td><td>982</td></tr>
    </tbody>
  </table>
</div>

<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2013">
  <table class="bnr-table">
    <thead>
      <tr>
        <th>Week of event (woe)</th>
        <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
      </tr>
      <tr>
        <th></th>
        <th>Stroke</th>
        <th>AMI</th>
        <th>Total</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>1</td><td>14</td><td>10</td><td>24</td></tr>
      <tr><td>2</td><td>17</td><td>9</td><td>26</td></tr>
      <tr><td>3</td><td>14</td><td>5</td><td>19</td></tr>
      <tr><td>4</td><td>17</td><td>9</td><td>26</td></tr>
      <tr><td>5</td><td>18</td><td>11</td><td>29</td></tr>
      <tr><td>6</td><td>16</td><td>11</td><td>27</td></tr>
      <tr><td>7</td><td>13</td><td>6</td><td>19</td></tr>
      <tr><td>8</td><td>13</td><td>8</td><td>21</td></tr>
      <tr><td>9</td><td>11</td><td>8</td><td>19</td></tr>
      <tr><td>10</td><td>17</td><td>3</td><td>20</td></tr>
      <tr><td>11</td><td>13</td><td>8</td><td>21</td></tr>
      <tr><td>12</td><td>15</td><td>8</td><td>23</td></tr>
      <tr><td>13</td><td>10</td><td>7</td><td>17</td></tr>
      <tr><td>14</td><td>14</td><td>5</td><td>19</td></tr>
      <tr><td>15</td><td>4</td><td>7</td><td>11</td></tr>
      <tr><td>16</td><td>15</td><td>3</td><td>18</td></tr>
      <tr><td>17</td><td>14</td><td>9</td><td>23</td></tr>
      <tr><td>18</td><td>7</td><td>5</td><td>12</td></tr>
      <tr><td>19</td><td>13</td><td>1</td><td>14</td></tr>
      <tr><td>20</td><td>7</td><td>12</td><td>19</td></tr>
      <tr><td>21</td><td>12</td><td>9</td><td>21</td></tr>
      <tr><td>22</td><td>16</td><td>7</td><td>23</td></tr>
      <tr><td>23</td><td>10</td><td>4</td><td>14</td></tr>
      <tr><td>24</td><td>8</td><td>7</td><td>15</td></tr>
      <tr><td>25</td><td>14</td><td>5</td><td>19</td></tr>
      <tr><td>26</td><td>17</td><td>5</td><td>22</td></tr>
      <tr><td>27</td><td>9</td><td>6</td><td>15</td></tr>
      <tr><td>28</td><td>11</td><td>11</td><td>22</td></tr>
      <tr><td>29</td><td>31</td><td>8</td><td>39</td></tr>
      <tr><td>30</td><td>16</td><td>6</td><td>22</td></tr>
      <tr><td>31</td><td>10</td><td>7</td><td>17</td></tr>
      <tr><td>32</td><td>15</td><td>10</td><td>25</td></tr>
      <tr><td>33</td><td>10</td><td>5</td><td>15</td></tr>
      <tr><td>34</td><td>14</td><td>9</td><td>23</td></tr>
      <tr><td>35</td><td>15</td><td>4</td><td>19</td></tr>
      <tr><td>36</td><td>11</td><td>5</td><td>16</td></tr>
      <tr><td>37</td><td>11</td><td>6</td><td>17</td></tr>
      <tr><td>38</td><td>12</td><td>2</td><td>14</td></tr>
      <tr><td>39</td><td>11</td><td>4</td><td>15</td></tr>
      <tr><td>40</td><td>23</td><td>7</td><td>30</td></tr>
      <tr><td>41</td><td>9</td><td>5</td><td>14</td></tr>
      <tr><td>42</td><td>12</td><td>10</td><td>22</td></tr>
      <tr><td>43</td><td>12</td><td>7</td><td>19</td></tr>
      <tr><td>44</td><td>17</td><td>8</td><td>25</td></tr>
      <tr><td>45</td><td>10</td><td>8</td><td>18</td></tr>
      <tr><td>46</td><td>11</td><td>2</td><td>13</td></tr>
      <tr><td>47</td><td>13</td><td>7</td><td>20</td></tr>
      <tr><td>48</td><td>16</td><td>9</td><td>25</td></tr>
      <tr><td>49</td><td>19</td><td>5</td><td>24</td></tr>
      <tr><td>50</td><td>13</td><td>10</td><td>23</td></tr>
      <tr><td>51</td><td>8</td><td>7</td><td>15</td></tr>
      <tr><td>52</td><td>16</td><td>2</td><td>18</td></tr>
      <tr><td>Total</td><td>694</td><td>352</td><td>1,046</td></tr>
    </tbody>
  </table>
</div>

  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2014">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>11</td><td>11</td><td>22</td></tr>
        <tr><td>2</td><td>10</td><td>10</td><td>20</td></tr>
        <tr><td>3</td><td>12</td><td>6</td><td>18</td></tr>
        <tr><td>4</td><td>10</td><td>7</td><td>17</td></tr>
        <tr><td>5</td><td>14</td><td>10</td><td>24</td></tr>
        <tr><td>6</td><td>6</td><td>5</td><td>11</td></tr>
        <tr><td>7</td><td>10</td><td>6</td><td>16</td></tr>
        <tr><td>8</td><td>9</td><td>5</td><td>14</td></tr>
        <tr><td>9</td><td>11</td><td>12</td><td>23</td></tr>
        <tr><td>10</td><td>13</td><td>9</td><td>22</td></tr>
        <tr><td>11</td><td>4</td><td>3</td><td>7</td></tr>
        <tr><td>12</td><td>9</td><td>9</td><td>18</td></tr>
        <tr><td>13</td><td>11</td><td>12</td><td>23</td></tr>
        <tr><td>14</td><td>8</td><td>4</td><td>12</td></tr>
        <tr><td>15</td><td>10</td><td>7</td><td>17</td></tr>
        <tr><td>16</td><td>19</td><td>9</td><td>28</td></tr>
        <tr><td>17</td><td>17</td><td>5</td><td>22</td></tr>
        <tr><td>18</td><td>11</td><td>5</td><td>16</td></tr>
        <tr><td>19</td><td>9</td><td>9</td><td>18</td></tr>
        <tr><td>20</td><td>6</td><td>8</td><td>14</td></tr>
        <tr><td>21</td><td>7</td><td>9</td><td>16</td></tr>
        <tr><td>22</td><td>7</td><td>4</td><td>11</td></tr>
        <tr><td>23</td><td>11</td><td>5</td><td>16</td></tr>
        <tr><td>24</td><td>11</td><td>2</td><td>13</td></tr>
        <tr><td>25</td><td>5</td><td>6</td><td>11</td></tr>
        <tr><td>26</td><td>15</td><td>8</td><td>23</td></tr>
        <tr><td>27</td><td>14</td><td>7</td><td>21</td></tr>
        <tr><td>28</td><td>6</td><td>6</td><td>12</td></tr>
        <tr><td>29</td><td>9</td><td>9</td><td>18</td></tr>
        <tr><td>30</td><td>14</td><td>10</td><td>24</td></tr>
        <tr><td>31</td><td>6</td><td>11</td><td>17</td></tr>
        <tr><td>32</td><td>17</td><td>5</td><td>22</td></tr>
        <tr><td>33</td><td>9</td><td>7</td><td>16</td></tr>
        <tr><td>34</td><td>11</td><td>10</td><td>21</td></tr>
        <tr><td>35</td><td>8</td><td>8</td><td>16</td></tr>
        <tr><td>36</td><td>10</td><td>6</td><td>16</td></tr>
        <tr><td>37</td><td>14</td><td>8</td><td>22</td></tr>
        <tr><td>38</td><td>16</td><td>8</td><td>24</td></tr>
        <tr><td>39</td><td>14</td><td>12</td><td>26</td></tr>
        <tr><td>40</td><td>11</td><td>7</td><td>18</td></tr>
        <tr><td>41</td><td>14</td><td>10</td><td>24</td></tr>
        <tr><td>42</td><td>16</td><td>5</td><td>21</td></tr>
        <tr><td>43</td><td>20</td><td>9</td><td>29</td></tr>
        <tr><td>44</td><td>17</td><td>12</td><td>29</td></tr>
        <tr><td>45</td><td>8</td><td>5</td><td>13</td></tr>
        <tr><td>46</td><td>3</td><td>8</td><td>11</td></tr>
        <tr><td>47</td><td>13</td><td>1</td><td>14</td></tr>
        <tr><td>48</td><td>10</td><td>16</td><td>26</td></tr>
        <tr><td>49</td><td>20</td><td>11</td><td>31</td></tr>
        <tr><td>50</td><td>14</td><td>11</td><td>25</td></tr>
        <tr><td>51</td><td>12</td><td>10</td><td>22</td></tr>
        <tr><td>52</td><td>12</td><td>12</td><td>24</td></tr>
        <tr><td>Total</td><td>584</td><td>410</td><td>994</td></tr>
      </tbody>
    </table>
  </div>
  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2015">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>12</td><td>12</td><td>24</td></tr>
        <tr><td>2</td><td>14</td><td>7</td><td>21</td></tr>
        <tr><td>3</td><td>16</td><td>7</td><td>23</td></tr>
        <tr><td>4</td><td>18</td><td>11</td><td>29</td></tr>
        <tr><td>5</td><td>12</td><td>7</td><td>19</td></tr>
        <tr><td>6</td><td>14</td><td>9</td><td>23</td></tr>
        <tr><td>7</td><td>19</td><td>11</td><td>30</td></tr>
        <tr><td>8</td><td>19</td><td>2</td><td>21</td></tr>
        <tr><td>9</td><td>9</td><td>11</td><td>20</td></tr>
        <tr><td>10</td><td>19</td><td>9</td><td>28</td></tr>
        <tr><td>11</td><td>18</td><td>8</td><td>26</td></tr>
        <tr><td>12</td><td>10</td><td>9</td><td>19</td></tr>
        <tr><td>13</td><td>6</td><td>8</td><td>14</td></tr>
        <tr><td>14</td><td>12</td><td>4</td><td>16</td></tr>
        <tr><td>15</td><td>7</td><td>7</td><td>14</td></tr>
        <tr><td>16</td><td>9</td><td>5</td><td>14</td></tr>
        <tr><td>17</td><td>11</td><td>8</td><td>19</td></tr>
        <tr><td>18</td><td>9</td><td>2</td><td>11</td></tr>
        <tr><td>19</td><td>10</td><td>3</td><td>13</td></tr>
        <tr><td>20</td><td>9</td><td>5</td><td>14</td></tr>
        <tr><td>21</td><td>9</td><td>5</td><td>14</td></tr>
        <tr><td>22</td><td>8</td><td>5</td><td>13</td></tr>
        <tr><td>23</td><td>10</td><td>5</td><td>15</td></tr>
        <tr><td>24</td><td>4</td><td>4</td><td>8</td></tr>
        <tr><td>25</td><td>7</td><td>2</td><td>9</td></tr>
        <tr><td>26</td><td>8</td><td>2</td><td>10</td></tr>
        <tr><td>27</td><td>5</td><td>6</td><td>11</td></tr>
        <tr><td>28</td><td>14</td><td>3</td><td>17</td></tr>
        <tr><td>29</td><td>16</td><td>4</td><td>20</td></tr>
        <tr><td>30</td><td>10</td><td>5</td><td>15</td></tr>
        <tr><td>31</td><td>8</td><td></td><td>8</td></tr>
        <tr><td>32</td><td>9</td><td>7</td><td>16</td></tr>
        <tr><td>33</td><td>4</td><td>6</td><td>10</td></tr>
        <tr><td>34</td><td>9</td><td>5</td><td>14</td></tr>
        <tr><td>35</td><td>8</td><td>1</td><td>9</td></tr>
        <tr><td>36</td><td>5</td><td>3</td><td>8</td></tr>
        <tr><td>37</td><td>9</td><td>2</td><td>11</td></tr>
        <tr><td>38</td><td>7</td><td>9</td><td>16</td></tr>
        <tr><td>39</td><td>16</td><td>6</td><td>22</td></tr>
        <tr><td>40</td><td>13</td><td>9</td><td>22</td></tr>
        <tr><td>41</td><td>8</td><td>9</td><td>17</td></tr>
        <tr><td>42</td><td>15</td><td>6</td><td>21</td></tr>
        <tr><td>43</td><td>9</td><td>10</td><td>19</td></tr>
        <tr><td>44</td><td>18</td><td>8</td><td>26</td></tr>
        <tr><td>45</td><td>17</td><td>5</td><td>22</td></tr>
        <tr><td>46</td><td>10</td><td>9</td><td>19</td></tr>
        <tr><td>47</td><td>14</td><td>10</td><td>24</td></tr>
        <tr><td>48</td><td>19</td><td>8</td><td>27</td></tr>
        <tr><td>49</td><td>5</td><td>9</td><td>14</td></tr>
        <tr><td>50</td><td>13</td><td>4</td><td>17</td></tr>
        <tr><td>51</td><td>13</td><td>9</td><td>22</td></tr>
        <tr><td>52</td><td>13</td><td>5</td><td>18</td></tr>
        <tr><td>Total</td><td>586</td><td>326</td><td>912</td></tr>
      </tbody>
    </table>
  </div>
  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2016">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>22</td><td>6</td><td>28</td></tr>
        <tr><td>2</td><td>19</td><td>12</td><td>31</td></tr>
        <tr><td>3</td><td>14</td><td>9</td><td>23</td></tr>
        <tr><td>4</td><td>19</td><td>7</td><td>26</td></tr>
        <tr><td>5</td><td>15</td><td>7</td><td>22</td></tr>
        <tr><td>6</td><td>14</td><td>5</td><td>19</td></tr>
        <tr><td>7</td><td>11</td><td>9</td><td>20</td></tr>
        <tr><td>8</td><td>14</td><td>8</td><td>22</td></tr>
        <tr><td>9</td><td>19</td><td>7</td><td>26</td></tr>
        <tr><td>10</td><td>15</td><td>2</td><td>17</td></tr>
        <tr><td>11</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>12</td><td>6</td><td>7</td><td>13</td></tr>
        <tr><td>13</td><td>16</td><td>4</td><td>20</td></tr>
        <tr><td>14</td><td>13</td><td>6</td><td>19</td></tr>
        <tr><td>15</td><td>15</td><td>6</td><td>21</td></tr>
        <tr><td>16</td><td>9</td><td>12</td><td>21</td></tr>
        <tr><td>17</td><td>15</td><td>9</td><td>24</td></tr>
        <tr><td>18</td><td>12</td><td>10</td><td>22</td></tr>
        <tr><td>19</td><td>15</td><td>7</td><td>22</td></tr>
        <tr><td>20</td><td>9</td><td>14</td><td>23</td></tr>
        <tr><td>21</td><td>10</td><td>14</td><td>24</td></tr>
        <tr><td>22</td><td>12</td><td>7</td><td>19</td></tr>
        <tr><td>23</td><td>14</td><td>12</td><td>26</td></tr>
        <tr><td>24</td><td>9</td><td>8</td><td>17</td></tr>
        <tr><td>25</td><td>7</td><td>9</td><td>16</td></tr>
        <tr><td>26</td><td>11</td><td>6</td><td>17</td></tr>
        <tr><td>27</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>28</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>29</td><td>12</td><td>11</td><td>23</td></tr>
        <tr><td>30</td><td>14</td><td>3</td><td>17</td></tr>
        <tr><td>31</td><td>12</td><td>9</td><td>21</td></tr>
        <tr><td>32</td><td>14</td><td>8</td><td>22</td></tr>
        <tr><td>33</td><td>12</td><td>10</td><td>22</td></tr>
        <tr><td>34</td><td>22</td><td>10</td><td>32</td></tr>
        <tr><td>35</td><td>14</td><td>9</td><td>23</td></tr>
        <tr><td>36</td><td>16</td><td>7</td><td>23</td></tr>
        <tr><td>37</td><td>15</td><td>10</td><td>25</td></tr>
        <tr><td>38</td><td>15</td><td>5</td><td>20</td></tr>
        <tr><td>39</td><td>13</td><td>8</td><td>21</td></tr>
        <tr><td>40</td><td>19</td><td>12</td><td>31</td></tr>
        <tr><td>41</td><td>12</td><td>7</td><td>19</td></tr>
        <tr><td>42</td><td>11</td><td>7</td><td>18</td></tr>
        <tr><td>43</td><td>14</td><td>7</td><td>21</td></tr>
        <tr><td>44</td><td>23</td><td>9</td><td>32</td></tr>
        <tr><td>45</td><td>15</td><td>11</td><td>26</td></tr>
        <tr><td>46</td><td>10</td><td>7</td><td>17</td></tr>
        <tr><td>47</td><td>11</td><td>10</td><td>21</td></tr>
        <tr><td>48</td><td>19</td><td>10</td><td>29</td></tr>
        <tr><td>49</td><td>18</td><td>5</td><td>23</td></tr>
        <tr><td>50</td><td>17</td><td>11</td><td>28</td></tr>
        <tr><td>51</td><td>11</td><td>8</td><td>19</td></tr>
        <tr><td>52</td><td>11</td><td>14</td><td>25</td></tr>
        <tr><td>Total</td><td>723</td><td>439</td><td>1,162</td></tr>
      </tbody>
    </table>
  </div>
  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2017">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>16</td><td>13</td><td>29</td></tr>
        <tr><td>2</td><td>12</td><td>16</td><td>28</td></tr>
        <tr><td>3</td><td>12</td><td>5</td><td>17</td></tr>
        <tr><td>4</td><td>17</td><td>12</td><td>29</td></tr>
        <tr><td>5</td><td>12</td><td>4</td><td>16</td></tr>
        <tr><td>6</td><td>17</td><td>15</td><td>32</td></tr>
        <tr><td>7</td><td>15</td><td>4</td><td>19</td></tr>
        <tr><td>8</td><td>9</td><td>8</td><td>17</td></tr>
        <tr><td>9</td><td>17</td><td>7</td><td>24</td></tr>
        <tr><td>10</td><td>12</td><td>6</td><td>18</td></tr>
        <tr><td>11</td><td>14</td><td>8</td><td>22</td></tr>
        <tr><td>12</td><td>17</td><td>10</td><td>27</td></tr>
        <tr><td>13</td><td>16</td><td>6</td><td>22</td></tr>
        <tr><td>14</td><td>10</td><td>9</td><td>19</td></tr>
        <tr><td>15</td><td>11</td><td>2</td><td>13</td></tr>
        <tr><td>16</td><td>16</td><td>8</td><td>24</td></tr>
        <tr><td>17</td><td>9</td><td>15</td><td>24</td></tr>
        <tr><td>18</td><td>14</td><td>7</td><td>21</td></tr>
        <tr><td>19</td><td>8</td><td>9</td><td>17</td></tr>
        <tr><td>20</td><td>18</td><td>12</td><td>30</td></tr>
        <tr><td>21</td><td>4</td><td>15</td><td>19</td></tr>
        <tr><td>22</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>23</td><td>7</td><td>6</td><td>13</td></tr>
        <tr><td>24</td><td>19</td><td>9</td><td>28</td></tr>
        <tr><td>25</td><td>21</td><td>6</td><td>27</td></tr>
        <tr><td>26</td><td>12</td><td>6</td><td>18</td></tr>
        <tr><td>27</td><td>10</td><td>10</td><td>20</td></tr>
        <tr><td>28</td><td>9</td><td>6</td><td>15</td></tr>
        <tr><td>29</td><td>14</td><td>11</td><td>25</td></tr>
        <tr><td>30</td><td>15</td><td>9</td><td>24</td></tr>
        <tr><td>31</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>32</td><td>14</td><td>14</td><td>28</td></tr>
        <tr><td>33</td><td>9</td><td>8</td><td>17</td></tr>
        <tr><td>34</td><td>11</td><td>6</td><td>17</td></tr>
        <tr><td>35</td><td>6</td><td>9</td><td>15</td></tr>
        <tr><td>36</td><td>7</td><td>10</td><td>17</td></tr>
        <tr><td>37</td><td>16</td><td>6</td><td>22</td></tr>
        <tr><td>38</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>39</td><td>13</td><td>8</td><td>21</td></tr>
        <tr><td>40</td><td>16</td><td>11</td><td>27</td></tr>
        <tr><td>41</td><td>7</td><td>9</td><td>16</td></tr>
        <tr><td>42</td><td>10</td><td>8</td><td>18</td></tr>
        <tr><td>43</td><td>9</td><td>13</td><td>22</td></tr>
        <tr><td>44</td><td>8</td><td>11</td><td>19</td></tr>
        <tr><td>45</td><td>10</td><td>9</td><td>19</td></tr>
        <tr><td>46</td><td>10</td><td>9</td><td>19</td></tr>
        <tr><td>47</td><td>19</td><td>13</td><td>32</td></tr>
        <tr><td>48</td><td>12</td><td>11</td><td>23</td></tr>
        <tr><td>49</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>50</td><td>10</td><td>13</td><td>23</td></tr>
        <tr><td>51</td><td>13</td><td>5</td><td>18</td></tr>
        <tr><td>52</td><td>18</td><td>6</td><td>24</td></tr>
        <tr><td>Total</td><td>650</td><td>467</td><td>1,117</td></tr>
      </tbody>
    </table>
  </div>
  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2018">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>18</td><td>12</td><td>30</td></tr>
        <tr><td>2</td><td>12</td><td>6</td><td>18</td></tr>
        <tr><td>3</td><td>17</td><td>7</td><td>24</td></tr>
        <tr><td>4</td><td>14</td><td>8</td><td>22</td></tr>
        <tr><td>5</td><td>14</td><td>7</td><td>21</td></tr>
        <tr><td>6</td><td>18</td><td>16</td><td>34</td></tr>
        <tr><td>7</td><td>24</td><td>8</td><td>32</td></tr>
        <tr><td>8</td><td>15</td><td>10</td><td>25</td></tr>
        <tr><td>9</td><td>11</td><td>13</td><td>24</td></tr>
        <tr><td>10</td><td>6</td><td>9</td><td>15</td></tr>
        <tr><td>11</td><td>14</td><td>12</td><td>26</td></tr>
        <tr><td>12</td><td>20</td><td>11</td><td>31</td></tr>
        <tr><td>13</td><td>12</td><td>12</td><td>24</td></tr>
        <tr><td>14</td><td>20</td><td>10</td><td>30</td></tr>
        <tr><td>15</td><td>21</td><td>10</td><td>31</td></tr>
        <tr><td>16</td><td>10</td><td>13</td><td>23</td></tr>
        <tr><td>17</td><td>8</td><td>14</td><td>22</td></tr>
        <tr><td>18</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>19</td><td>17</td><td>12</td><td>29</td></tr>
        <tr><td>20</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>21</td><td>14</td><td>9</td><td>23</td></tr>
        <tr><td>22</td><td>11</td><td>9</td><td>20</td></tr>
        <tr><td>23</td><td>12</td><td>7</td><td>19</td></tr>
        <tr><td>24</td><td>12</td><td>11</td><td>23</td></tr>
        <tr><td>25</td><td>10</td><td>10</td><td>20</td></tr>
        <tr><td>26</td><td>11</td><td>12</td><td>23</td></tr>
        <tr><td>27</td><td>6</td><td>14</td><td>20</td></tr>
        <tr><td>28</td><td>13</td><td>7</td><td>20</td></tr>
        <tr><td>29</td><td>11</td><td>9</td><td>20</td></tr>
        <tr><td>30</td><td>14</td><td>7</td><td>21</td></tr>
        <tr><td>31</td><td>11</td><td>6</td><td>17</td></tr>
        <tr><td>32</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>33</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>34</td><td>17</td><td>5</td><td>22</td></tr>
        <tr><td>35</td><td>11</td><td>4</td><td>15</td></tr>
        <tr><td>36</td><td>17</td><td>4</td><td>21</td></tr>
        <tr><td>37</td><td>10</td><td>4</td><td>14</td></tr>
        <tr><td>38</td><td>10</td><td>8</td><td>18</td></tr>
        <tr><td>39</td><td>18</td><td>8</td><td>26</td></tr>
        <tr><td>40</td><td>7</td><td>17</td><td>24</td></tr>
        <tr><td>41</td><td>12</td><td>14</td><td>26</td></tr>
        <tr><td>42</td><td>10</td><td>11</td><td>21</td></tr>
        <tr><td>43</td><td>8</td><td>6</td><td>14</td></tr>
        <tr><td>44</td><td>12</td><td>5</td><td>17</td></tr>
        <tr><td>45</td><td>12</td><td>13</td><td>25</td></tr>
        <tr><td>46</td><td>9</td><td>16</td><td>25</td></tr>
        <tr><td>47</td><td>12</td><td>11</td><td>23</td></tr>
        <tr><td>48</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>49</td><td>17</td><td>6</td><td>23</td></tr>
        <tr><td>50</td><td>17</td><td>5</td><td>22</td></tr>
        <tr><td>51</td><td>9</td><td>7</td><td>16</td></tr>
        <tr><td>52</td><td>15</td><td>2</td><td>17</td></tr>
        <tr><td>Total</td><td>682</td><td>483</td><td>1,165</td></tr>
      </tbody>
    </table>
  </div>
  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2019">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>18</td><td>13</td><td>31</td></tr>
        <tr><td>2</td><td>19</td><td>14</td><td>33</td></tr>
        <tr><td>3</td><td>12</td><td>11</td><td>23</td></tr>
        <tr><td>4</td><td>18</td><td>11</td><td>29</td></tr>
        <tr><td>5</td><td>28</td><td>15</td><td>43</td></tr>
        <tr><td>6</td><td>14</td><td>10</td><td>24</td></tr>
        <tr><td>7</td><td>21</td><td>12</td><td>33</td></tr>
        <tr><td>8</td><td>14</td><td>5</td><td>19</td></tr>
        <tr><td>9</td><td>19</td><td>15</td><td>34</td></tr>
        <tr><td>10</td><td>20</td><td>6</td><td>26</td></tr>
        <tr><td>11</td><td>14</td><td>10</td><td>24</td></tr>
        <tr><td>12</td><td>20</td><td>8</td><td>28</td></tr>
        <tr><td>13</td><td>12</td><td>10</td><td>22</td></tr>
        <tr><td>14</td><td>16</td><td>10</td><td>26</td></tr>
        <tr><td>15</td><td>18</td><td>11</td><td>29</td></tr>
        <tr><td>16</td><td>14</td><td>6</td><td>20</td></tr>
        <tr><td>17</td><td>10</td><td>14</td><td>24</td></tr>
        <tr><td>18</td><td>19</td><td>11</td><td>30</td></tr>
        <tr><td>19</td><td>16</td><td>12</td><td>28</td></tr>
        <tr><td>20</td><td>13</td><td>11</td><td>24</td></tr>
        <tr><td>21</td><td>18</td><td>16</td><td>34</td></tr>
        <tr><td>22</td><td>14</td><td>10</td><td>24</td></tr>
        <tr><td>23</td><td>22</td><td>11</td><td>33</td></tr>
        <tr><td>24</td><td>15</td><td>9</td><td>24</td></tr>
        <tr><td>25</td><td>16</td><td>11</td><td>27</td></tr>
        <tr><td>26</td><td>9</td><td>8</td><td>17</td></tr>
        <tr><td>27</td><td>14</td><td>11</td><td>25</td></tr>
        <tr><td>28</td><td>8</td><td>10</td><td>18</td></tr>
        <tr><td>29</td><td>11</td><td>12</td><td>23</td></tr>
        <tr><td>30</td><td>14</td><td>5</td><td>19</td></tr>
        <tr><td>31</td><td>14</td><td>9</td><td>23</td></tr>
        <tr><td>32</td><td>16</td><td>10</td><td>26</td></tr>
        <tr><td>33</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>34</td><td>14</td><td>3</td><td>17</td></tr>
        <tr><td>35</td><td>17</td><td>8</td><td>25</td></tr>
        <tr><td>36</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>37</td><td>15</td><td>17</td><td>32</td></tr>
        <tr><td>38</td><td>19</td><td>19</td><td>38</td></tr>
        <tr><td>39</td><td>9</td><td>17</td><td>26</td></tr>
        <tr><td>40</td><td>14</td><td>9</td><td>23</td></tr>
        <tr><td>41</td><td>14</td><td>7</td><td>21</td></tr>
        <tr><td>42</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>43</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>44</td><td>6</td><td>8</td><td>14</td></tr>
        <tr><td>45</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>46</td><td>14</td><td>4</td><td>18</td></tr>
        <tr><td>47</td><td>12</td><td>12</td><td>24</td></tr>
        <tr><td>48</td><td>14</td><td>15</td><td>29</td></tr>
        <tr><td>49</td><td>8</td><td>10</td><td>18</td></tr>
        <tr><td>50</td><td>10</td><td>7</td><td>17</td></tr>
        <tr><td>51</td><td>14</td><td>13</td><td>27</td></tr>
        <tr><td>52</td><td>10</td><td>17</td><td>27</td></tr>
        <tr><td>Total</td><td>758</td><td>547</td><td>1,305</td></tr>
      </tbody>
    </table>
  </div>
  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2020">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>11</td><td>14</td><td>25</td></tr>
        <tr><td>2</td><td>12</td><td>11</td><td>23</td></tr>
        <tr><td>3</td><td>12</td><td>10</td><td>22</td></tr>
        <tr><td>4</td><td>18</td><td>10</td><td>28</td></tr>
        <tr><td>5</td><td>18</td><td>18</td><td>36</td></tr>
        <tr><td>6</td><td>18</td><td>10</td><td>28</td></tr>
        <tr><td>7</td><td>11</td><td>19</td><td>30</td></tr>
        <tr><td>8</td><td>16</td><td>15</td><td>31</td></tr>
        <tr><td>9</td><td>18</td><td>16</td><td>34</td></tr>
        <tr><td>10</td><td>9</td><td>10</td><td>19</td></tr>
        <tr><td>11</td><td>17</td><td>11</td><td>28</td></tr>
        <tr><td>12</td><td>6</td><td>7</td><td>13</td></tr>
        <tr><td>13</td><td>12</td><td>11</td><td>23</td></tr>
        <tr><td>14</td><td>10</td><td>10</td><td>20</td></tr>
        <tr><td>15</td><td>12</td><td>9</td><td>21</td></tr>
        <tr><td>16</td><td>15</td><td>12</td><td>27</td></tr>
        <tr><td>17</td><td>18</td><td>11</td><td>29</td></tr>
        <tr><td>18</td><td>13</td><td>14</td><td>27</td></tr>
        <tr><td>19</td><td>7</td><td>6</td><td>13</td></tr>
        <tr><td>20</td><td>25</td><td>13</td><td>38</td></tr>
        <tr><td>21</td><td>7</td><td>10</td><td>17</td></tr>
        <tr><td>22</td><td>14</td><td>10</td><td>24</td></tr>
        <tr><td>23</td><td>7</td><td>11</td><td>18</td></tr>
        <tr><td>24</td><td>8</td><td>10</td><td>18</td></tr>
        <tr><td>25</td><td>16</td><td>7</td><td>23</td></tr>
        <tr><td>26</td><td>16</td><td>13</td><td>29</td></tr>
        <tr><td>27</td><td>17</td><td>13</td><td>30</td></tr>
        <tr><td>28</td><td>12</td><td>12</td><td>24</td></tr>
        <tr><td>29</td><td>8</td><td>13</td><td>21</td></tr>
        <tr><td>30</td><td>12</td><td>10</td><td>22</td></tr>
        <tr><td>31</td><td>20</td><td>13</td><td>33</td></tr>
        <tr><td>32</td><td>17</td><td>1</td><td>18</td></tr>
        <tr><td>33</td><td>8</td><td>8</td><td>16</td></tr>
        <tr><td>34</td><td>16</td><td>14</td><td>30</td></tr>
        <tr><td>35</td><td>19</td><td>8</td><td>27</td></tr>
        <tr><td>36</td><td>12</td><td>6</td><td>18</td></tr>
        <tr><td>37</td><td>17</td><td>9</td><td>26</td></tr>
        <tr><td>38</td><td>13</td><td>12</td><td>25</td></tr>
        <tr><td>39</td><td>13</td><td>12</td><td>25</td></tr>
        <tr><td>40</td><td>12</td><td>8</td><td>20</td></tr>
        <tr><td>41</td><td>12</td><td>3</td><td>15</td></tr>
        <tr><td>42</td><td>13</td><td>9</td><td>22</td></tr>
        <tr><td>43</td><td>10</td><td>13</td><td>23</td></tr>
        <tr><td>44</td><td>14</td><td>8</td><td>22</td></tr>
        <tr><td>45</td><td>9</td><td>5</td><td>14</td></tr>
        <tr><td>46</td><td>7</td><td>9</td><td>16</td></tr>
        <tr><td>47</td><td>19</td><td>14</td><td>33</td></tr>
        <tr><td>48</td><td>11</td><td>10</td><td>21</td></tr>
        <tr><td>49</td><td>12</td><td>9</td><td>21</td></tr>
        <tr><td>50</td><td>15</td><td>11</td><td>26</td></tr>
        <tr><td>51</td><td>16</td><td>3</td><td>19</td></tr>
        <tr><td>52</td><td>19</td><td>16</td><td>35</td></tr>
        <tr><td>Total</td><td>699</td><td>547</td><td>1,246</td></tr>
      </tbody>
    </table>
  </div>
  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2021">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>15</td><td>10</td><td>25</td></tr>
        <tr><td>2</td><td>11</td><td>7</td><td>18</td></tr>
        <tr><td>3</td><td>15</td><td>9</td><td>24</td></tr>
        <tr><td>4</td><td>9</td><td>13</td><td>22</td></tr>
        <tr><td>5</td><td>16</td><td>10</td><td>26</td></tr>
        <tr><td>6</td><td>14</td><td>6</td><td>20</td></tr>
        <tr><td>7</td><td>21</td><td>11</td><td>32</td></tr>
        <tr><td>8</td><td>9</td><td>12</td><td>21</td></tr>
        <tr><td>9</td><td>16</td><td>4</td><td>20</td></tr>
        <tr><td>10</td><td>10</td><td>11</td><td>21</td></tr>
        <tr><td>11</td><td>9</td><td>3</td><td>12</td></tr>
        <tr><td>12</td><td>15</td><td>8</td><td>23</td></tr>
        <tr><td>13</td><td>10</td><td>7</td><td>17</td></tr>
        <tr><td>14</td><td>7</td><td>6</td><td>13</td></tr>
        <tr><td>15</td><td>8</td><td>11</td><td>19</td></tr>
        <tr><td>16</td><td>10</td><td>5</td><td>15</td></tr>
        <tr><td>17</td><td>7</td><td>10</td><td>17</td></tr>
        <tr><td>18</td><td>18</td><td>8</td><td>26</td></tr>
        <tr><td>19</td><td>18</td><td>7</td><td>25</td></tr>
        <tr><td>20</td><td>17</td><td>8</td><td>25</td></tr>
        <tr><td>21</td><td>11</td><td>12</td><td>23</td></tr>
        <tr><td>22</td><td>12</td><td>5</td><td>17</td></tr>
        <tr><td>23</td><td>9</td><td>4</td><td>13</td></tr>
        <tr><td>24</td><td>7</td><td>4</td><td>11</td></tr>
        <tr><td>25</td><td>10</td><td>7</td><td>17</td></tr>
        <tr><td>26</td><td>13</td><td>3</td><td>16</td></tr>
        <tr><td>27</td><td>25</td><td>13</td><td>38</td></tr>
        <tr><td>28</td><td>17</td><td>14</td><td>31</td></tr>
        <tr><td>29</td><td>8</td><td>13</td><td>21</td></tr>
        <tr><td>30</td><td>16</td><td>11</td><td>27</td></tr>
        <tr><td>31</td><td>22</td><td>14</td><td>36</td></tr>
        <tr><td>32</td><td>17</td><td>11</td><td>28</td></tr>
        <tr><td>33</td><td>4</td><td>11</td><td>15</td></tr>
        <tr><td>34</td><td>19</td><td>7</td><td>26</td></tr>
        <tr><td>35</td><td>14</td><td>8</td><td>22</td></tr>
        <tr><td>36</td><td>13</td><td>18</td><td>31</td></tr>
        <tr><td>37</td><td>13</td><td>9</td><td>22</td></tr>
        <tr><td>38</td><td>12</td><td>11</td><td>23</td></tr>
        <tr><td>39</td><td>22</td><td>15</td><td>37</td></tr>
        <tr><td>40</td><td>15</td><td>9</td><td>24</td></tr>
        <tr><td>41</td><td>18</td><td>7</td><td>25</td></tr>
        <tr><td>42</td><td>10</td><td>14</td><td>24</td></tr>
        <tr><td>43</td><td>8</td><td>12</td><td>20</td></tr>
        <tr><td>44</td><td>17</td><td>6</td><td>23</td></tr>
        <tr><td>45</td><td>12</td><td>10</td><td>22</td></tr>
        <tr><td>46</td><td>14</td><td>9</td><td>23</td></tr>
        <tr><td>47</td><td>12</td><td>13</td><td>25</td></tr>
        <tr><td>48</td><td>15</td><td>4</td><td>19</td></tr>
        <tr><td>49</td><td>10</td><td>5</td><td>15</td></tr>
        <tr><td>50</td><td>9</td><td>6</td><td>15</td></tr>
        <tr><td>51</td><td>17</td><td>6</td><td>23</td></tr>
        <tr><td>52</td><td>15</td><td>10</td><td>25</td></tr>
        <tr><td>Total</td><td>691</td><td>467</td><td>1,158</td></tr>
      </tbody>
    </table>
  </div>
  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2022">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>24</td><td>10</td><td>34</td></tr>
        <tr><td>2</td><td>10</td><td>12</td><td>22</td></tr>
        <tr><td>3</td><td>17</td><td>8</td><td>25</td></tr>
        <tr><td>4</td><td>18</td><td>15</td><td>33</td></tr>
        <tr><td>5</td><td>20</td><td>11</td><td>31</td></tr>
        <tr><td>6</td><td>22</td><td>21</td><td>43</td></tr>
        <tr><td>7</td><td>18</td><td>11</td><td>29</td></tr>
        <tr><td>8</td><td>21</td><td>15</td><td>36</td></tr>
        <tr><td>9</td><td>17</td><td>14</td><td>31</td></tr>
        <tr><td>10</td><td>8</td><td>18</td><td>26</td></tr>
        <tr><td>11</td><td>12</td><td>13</td><td>25</td></tr>
        <tr><td>12</td><td>19</td><td>5</td><td>24</td></tr>
        <tr><td>13</td><td>8</td><td>12</td><td>20</td></tr>
        <tr><td>14</td><td>12</td><td>7</td><td>19</td></tr>
        <tr><td>15</td><td>16</td><td>15</td><td>31</td></tr>
        <tr><td>16</td><td>14</td><td>15</td><td>29</td></tr>
        <tr><td>17</td><td>13</td><td>12</td><td>25</td></tr>
        <tr><td>18</td><td>11</td><td>11</td><td>22</td></tr>
        <tr><td>19</td><td>10</td><td>3</td><td>13</td></tr>
        <tr><td>20</td><td>7</td><td>13</td><td>20</td></tr>
        <tr><td>21</td><td>14</td><td>16</td><td>30</td></tr>
        <tr><td>22</td><td>15</td><td>11</td><td>26</td></tr>
        <tr><td>23</td><td>17</td><td>9</td><td>26</td></tr>
        <tr><td>24</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>25</td><td>15</td><td>9</td><td>24</td></tr>
        <tr><td>26</td><td>12</td><td>10</td><td>22</td></tr>
        <tr><td>27</td><td>14</td><td>10</td><td>24</td></tr>
        <tr><td>28</td><td>16</td><td>9</td><td>25</td></tr>
        <tr><td>29</td><td>16</td><td>13</td><td>29</td></tr>
        <tr><td>30</td><td>15</td><td>9</td><td>24</td></tr>
        <tr><td>31</td><td>8</td><td>11</td><td>19</td></tr>
        <tr><td>32</td><td>15</td><td>9</td><td>24</td></tr>
        <tr><td>33</td><td>13</td><td>11</td><td>24</td></tr>
        <tr><td>34</td><td>23</td><td>12</td><td>35</td></tr>
        <tr><td>35</td><td>12</td><td>13</td><td>25</td></tr>
        <tr><td>36</td><td>13</td><td>9</td><td>22</td></tr>
        <tr><td>37</td><td>16</td><td>13</td><td>29</td></tr>
        <tr><td>38</td><td>19</td><td>12</td><td>31</td></tr>
        <tr><td>39</td><td>11</td><td>5</td><td>16</td></tr>
        <tr><td>40</td><td>18</td><td>8</td><td>26</td></tr>
        <tr><td>41</td><td>24</td><td>10</td><td>34</td></tr>
        <tr><td>42</td><td>14</td><td>13</td><td>27</td></tr>
        <tr><td>43</td><td>16</td><td>9</td><td>25</td></tr>
        <tr><td>44</td><td>14</td><td>9</td><td>23</td></tr>
        <tr><td>45</td><td>15</td><td>15</td><td>30</td></tr>
        <tr><td>46</td><td>17</td><td>10</td><td>27</td></tr>
        <tr><td>47</td><td>17</td><td>7</td><td>24</td></tr>
        <tr><td>48</td><td>10</td><td>12</td><td>22</td></tr>
        <tr><td>49</td><td>11</td><td>10</td><td>21</td></tr>
        <tr><td>50</td><td>14</td><td>7</td><td>21</td></tr>
        <tr><td>51</td><td>14</td><td>8</td><td>22</td></tr>
        <tr><td>52</td><td>10</td><td>10</td><td>20</td></tr>
        <tr><td>Total</td><td>768</td><td>570</td><td>1,338</td></tr>
      </tbody>
    </table>
  </div>
  <div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2023">
    <table class="bnr-table">
      <thead>
        <tr>
          <th>Week of event (woe)</th>
          <th colspan="3">CVD Event Type (AMI=2, Stroke=1)</th>
        </tr>
        <tr>
          <th></th>
          <th>Stroke</th>
          <th>AMI</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>15</td><td>11</td><td>26</td></tr>
        <tr><td>2</td><td>23</td><td>18</td><td>41</td></tr>
        <tr><td>3</td><td>23</td><td>11</td><td>34</td></tr>
        <tr><td>4</td><td>18</td><td>11</td><td>29</td></tr>
        <tr><td>5</td><td>18</td><td>10</td><td>28</td></tr>
        <tr><td>6</td><td>19</td><td>8</td><td>27</td></tr>
        <tr><td>7</td><td>18</td><td>9</td><td>27</td></tr>
        <tr><td>8</td><td>15</td><td>9</td><td>24</td></tr>
        <tr><td>9</td><td>17</td><td>12</td><td>29</td></tr>
        <tr><td>10</td><td>17</td><td>11</td><td>28</td></tr>
        <tr><td>11</td><td>19</td><td>11</td><td>30</td></tr>
        <tr><td>12</td><td>13</td><td>11</td><td>24</td></tr>
        <tr><td>13</td><td>9</td><td>9</td><td>18</td></tr>
        <tr><td>14</td><td>17</td><td>12</td><td>29</td></tr>
        <tr><td>15</td><td>12</td><td>14</td><td>26</td></tr>
        <tr><td>16</td><td>15</td><td>16</td><td>31</td></tr>
        <tr><td>17</td><td>19</td><td>7</td><td>26</td></tr>
        <tr><td>18</td><td>17</td><td>14</td><td>31</td></tr>
        <tr><td>19</td><td>19</td><td>6</td><td>25</td></tr>
        <tr><td>20</td><td>19</td><td>11</td><td>30</td></tr>
        <tr><td>21</td><td>21</td><td>10</td><td>31</td></tr>
        <tr><td>22</td><td>20</td><td>9</td><td>29</td></tr>
        <tr><td>23</td><td>15</td><td>14</td><td>29</td></tr>
        <tr><td>24</td><td>21</td><td>6</td><td>27</td></tr>
        <tr><td>25</td><td>9</td><td>7</td><td>16</td></tr>
        <tr><td>26</td><td>17</td><td>8</td><td>25</td></tr>
        <tr><td>27</td><td>16</td><td>12</td><td>28</td></tr>
        <tr><td>28</td><td>18</td><td>5</td><td>23</td></tr>
        <tr><td>29</td><td>15</td><td>12</td><td>27</td></tr>
        <tr><td>30</td><td>10</td><td>10</td><td>20</td></tr>
        <tr><td>31</td><td>20</td><td>10</td><td>30</td></tr>
        <tr><td>32</td><td>18</td><td>15</td><td>33</td></tr>
        <tr><td>33</td><td>10</td><td>8</td><td>18</td></tr>
        <tr><td>34</td><td>15</td><td>11</td><td>26</td></tr>
        <tr><td>35</td><td>12</td><td>6</td><td>18</td></tr>
        <tr><td>36</td><td>14</td><td>8</td><td>22</td></tr>
        <tr><td>37</td><td>16</td><td>11</td><td>27</td></tr>
        <tr><td>38</td><td>19</td><td>15</td><td>34</td></tr>
        <tr><td>39</td><td>10</td><td>12</td><td>22</td></tr>
        <tr><td>40</td><td>10</td><td>17</td><td>27</td></tr>
        <tr><td>41</td><td>9</td><td>12</td><td>21</td></tr>
        <tr><td>42</td><td>15</td><td>10</td><td>25</td></tr>
        <tr><td>43</td><td>5</td><td>10</td><td>15</td></tr>
        <tr><td>44</td><td>8</td><td>13</td><td>21</td></tr>
        <tr><td>45</td><td>9</td><td>8</td><td>17</td></tr>
        <tr><td>46</td><td>10</td><td>11</td><td>21</td></tr>
        <tr><td>47</td><td>19</td><td>10</td><td>29</td></tr>
        <tr><td>48</td><td>19</td><td>14</td><td>33</td></tr>
        <tr><td>49</td><td>13</td><td>10</td><td>23</td></tr>
        <tr><td>50</td><td>20</td><td>9</td><td>29</td></tr>
        <tr><td>51</td><td>13</td><td>12</td><td>25</td></tr>
        <tr><td>52</td><td>15</td><td>18</td><td>33</td></tr>
        <tr><td>Total</td><td>803</td><td>564</td><td>1,367</td></tr>
      </tbody>
    </table>
  </div>
</div>

[Download Data](../downloads/data/bnr-cvd-2023-table2.xlsx){ .md-button .btn-right}
<br/><br/>

---

## **Table 3.** Event Percentage among Younger Adults (<70 years) and Older Adults (70+ years)  
### 2023 compared to the previous 5 years (2018-2022)
<div class="bnr-table-wrapper">
  <table class="bnr-table">
    <thead>
      <tr>
        <th rowspan="3">Time period / patient age group</th>
        <th colspan="2">Stroke</th>
        <th colspan="2">AMI</th>
      </tr>
      <tr>
        <th colspan="2">Patient sex</th>
        <th colspan="2">Patient sex</th>
      </tr>
      <tr>
        <th>Female (%)</th>
        <th>Male (%)</th>
        <th>Female (%)</th>
        <th>Male (%)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td colspan="5"><strong>Average (2018–2022)</strong></td>
      </tr>
      <tr>
        <td><em>Patient age group (&lt;70 yrs; 70+ yrs)</em></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>&lt;70 years</td>
        <td>35.1</td>
        <td>50.3</td>
        <td>30.9</td>
        <td>51.2</td>
      </tr>
      <tr>
        <td>70 years and older</td>
        <td>64.9</td>
        <td>49.7</td>
        <td>69.1</td>
        <td>48.8</td>
      </tr>
      <tr>
        <td colspan="5"><strong>2023</strong></td>
      </tr>
      <tr>
        <td><em>Patient age group (&lt;70 yrs; 70+ yrs)</em></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>&lt;70 years</td>
        <td>31.4</td>
        <td>51.0</td>
        <td>31.8</td>
        <td>52.5</td>
      </tr>
      <tr>
        <td>70 years and older</td>
        <td>68.6</td>
        <td>49.0</td>
        <td>68.2</td>
        <td>47.5</td>
      </tr>
    </tbody>
  </table>
</div>

[Download Data](../downloads/data/bnr-cvd-2023-table3.xlsx){ .md-button .btn-right}
<br/><br/>

---

## **Table 4.** Event Percentage by 10-Year Age Groups  
### 2023 compared to the previous 5 years (2018-2022)
<div class="bnr-table-wrapper">
  <table class="bnr-table">
    <thead>
      <tr>
        <th rowspan="3">Time period / patient age group</th>
        <th colspan="3">Stroke</th>
        <th colspan="3">AMI</th>
      </tr>
      <tr>
        <th colspan="3">Patient sex</th>
        <th colspan="3">Patient sex</th>
      </tr>
      <tr>
        <th>Female (%)</th>
        <th>Male (%)</th>
        <th>All (%)</th>
        <th>Female (%)</th>
        <th>Male (%)</th>
        <th>All (%)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td colspan="7"><strong>Average (2018&ndash;2022)</strong></td>
      </tr>
      <tr>
        <td><em>Patient age group (years)</em></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>&lt;40</td>
        <td>2.2</td>
        <td>2.6</td>
        <td>2.4</td>
        <td>1.1</td>
        <td>2.5</td>
        <td>1.8</td>
      </tr>
      <tr>
        <td>40&ndash;49</td>
        <td>6.2</td>
        <td>5.0</td>
        <td>5.6</td>
        <td>4.1</td>
        <td>7.2</td>
        <td>5.7</td>
      </tr>
      <tr>
        <td>50&ndash;59</td>
        <td>10.2</td>
        <td>15.1</td>
        <td>12.6</td>
        <td>9.3</td>
        <td>14.9</td>
        <td>12.3</td>
      </tr>
      <tr>
        <td>60&ndash;69</td>
        <td>16.5</td>
        <td>27.6</td>
        <td>21.9</td>
        <td>16.3</td>
        <td>26.7</td>
        <td>21.8</td>
      </tr>
      <tr>
        <td>70&ndash;79</td>
        <td>22.1</td>
        <td>27.3</td>
        <td>24.6</td>
        <td>20.4</td>
        <td>23.8</td>
        <td>22.2</td>
      </tr>
      <tr>
        <td>80+</td>
        <td>42.8</td>
        <td>22.3</td>
        <td>32.9</td>
        <td>48.7</td>
        <td>25.0</td>
        <td>36.2</td>
      </tr>

      <tr>
        <td colspan="7"><strong>2023</strong></td>
      </tr>
      <tr>
        <td><em>Patient age group (years)</em></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>&lt;40</td>
        <td>2.0</td>
        <td>2.0</td>
        <td>2.0</td>
        <td>1.9</td>
        <td>1.0</td>
        <td>1.4</td>
      </tr>
      <tr>
        <td>40&ndash;49</td>
        <td>5.2</td>
        <td>5.6</td>
        <td>5.4</td>
        <td>4.1</td>
        <td>6.4</td>
        <td>5.3</td>
      </tr>
      <tr>
        <td>50&ndash;59</td>
        <td>8.8</td>
        <td>20.2</td>
        <td>14.4</td>
        <td>7.9</td>
        <td>19.5</td>
        <td>14.0</td>
      </tr>
      <tr>
        <td>60&ndash;69</td>
        <td>15.5</td>
        <td>23.2</td>
        <td>19.3</td>
        <td>18.0</td>
        <td>25.6</td>
        <td>22.0</td>
      </tr>
      <tr>
        <td>70&ndash;79</td>
        <td>28.7</td>
        <td>25.0</td>
        <td>26.9</td>
        <td>20.6</td>
        <td>26.6</td>
        <td>23.8</td>
      </tr>
      <tr>
        <td>80+</td>
        <td>39.8</td>
        <td>24.0</td>
        <td>32.0</td>
        <td>47.6</td>
        <td>20.9</td>
        <td>33.5</td>
      </tr>
    </tbody>
  </table>
</div>


[Download Data](../downloads/data/bnr-cvd-2023-table4.xlsx){ .md-button .btn-right}
<br/><br/>

---



---

## **Table 5.** CVD Incidence Rates (2010 to 2023)   

### Incidence Rates for Hospital Events and for Hospital Events and "Deaths Certificate Only" events Combined  

### Rates Age Adjusted Using the WHO Standard World Population

<div class="bnr-year-block">
<label class="bnr-year-label">Select year:</label>
<select class="bnr-year-select">
<option value="2010">2010</option>
<option value="2011">2011</option>
<option value="2012">2012</option>
<option value="2013">2013</option>
<option value="2014">2014</option>
<option value="2015">2015</option>
<option value="2016">2016</option>
<option value="2017">2017</option>
<option value="2018">2018</option>
<option value="2019">2019</option>
<option value="2020">2020</option>
<option value="2021">2021</option>
<option value="2022">2022</option>
<option value="2023" selected>2023</option>
</select>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2010"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2010</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>157.2</td><td>154.4</td><td>155.9</td><td>41.7</td><td>50.2</td><td>45.8</td></tr>
<tr><td>Adjusted rate</td><td>95.2</td><td>122.9</td><td>108.2</td><td>26.8</td><td>39.9</td><td>32.9</td></tr>
<tr><td>Lower 95% Limit</td><td>82.8</td><td>106.5</td><td>98.1</td><td>20.2</td><td>30.8</td><td>27.3</td></tr>
<tr><td>Upper 95% Limit</td><td>109.2</td><td>141.3</td><td>119.2</td><td>34.9</td><td>50.9</td><td>39.3</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>223.3</td><td>197.8</td><td>211.1</td><td>124.5</td><td>125.5</td><td>125.0</td></tr>
<tr><td>Adjusted rate</td><td>129.8</td><td>158.4</td><td>143.8</td><td>73.5</td><td>100.3</td><td>85.9</td></tr>
<tr><td>Lower 95% Limit</td><td>115.6</td><td>139.6</td><td>132.1</td><td>62.8</td><td>85.5</td><td>76.9</td></tr>
<tr><td>Upper 95% Limit</td><td>145.7</td><td>179.1</td><td>156.2</td><td>85.8</td><td>117.0</td><td>95.8</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2011"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2011</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>139.4</td><td>139.4</td><td>139.4</td><td>31.2</td><td>56.1</td><td>43.1</td></tr>
<tr><td>Adjusted rate</td><td>87.0</td><td>109.3</td><td>97.1</td><td>20.7</td><td>44.4</td><td>31.5</td></tr>
<tr><td>Lower 95% Limit</td><td>75.0</td><td>94.0</td><td>87.5</td><td>15.0</td><td>34.8</td><td>26.1</td></tr>
<tr><td>Upper 95% Limit</td><td>100.5</td><td>126.5</td><td>107.5</td><td>28.2</td><td>55.9</td><td>37.9</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>209.5</td><td>197.8</td><td>203.9</td><td>87.4</td><td>127.3</td><td>106.5</td></tr>
<tr><td>Adjusted rate</td><td>124.0</td><td>155.4</td><td>138.8</td><td>50.7</td><td>101.0</td><td>73.1</td></tr>
<tr><td>Lower 95% Limit</td><td>109.9</td><td>137.0</td><td>127.4</td><td>42.0</td><td>86.2</td><td>64.8</td></tr>
<tr><td>Upper 95% Limit</td><td>139.5</td><td>175.7</td><td>151.0</td><td>61.1</td><td>117.7</td><td>82.2</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2012"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2012</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>139.8</td><td>147.3</td><td>143.4</td><td>66.4</td><td>68.7</td><td>67.5</td></tr>
<tr><td>Adjusted rate</td><td>84.0</td><td>114.6</td><td>97.5</td><td>40.9</td><td>53.3</td><td>46.5</td></tr>
<tr><td>Lower 95% Limit</td><td>72.5</td><td>99.0</td><td>88.0</td><td>32.9</td><td>42.8</td><td>40.0</td></tr>
<tr><td>Upper 95% Limit</td><td>97.0</td><td>132.1</td><td>107.8</td><td>50.4</td><td>65.6</td><td>53.9</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>222.1</td><td>194.1</td><td>208.7</td><td>139.1</td><td>153.3</td><td>145.9</td></tr>
<tr><td>Adjusted rate</td><td>126.0</td><td>150.4</td><td>137.9</td><td>80.9</td><td>119.7</td><td>98.4</td></tr>
<tr><td>Lower 95% Limit</td><td>112.2</td><td>132.5</td><td>126.7</td><td>69.7</td><td>103.7</td><td>88.9</td></tr>
<tr><td>Upper 95% Limit</td><td>141.3</td><td>170.2</td><td>149.9</td><td>93.5</td><td>137.6</td><td>108.7</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2013"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2013</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>191.9</td><td>200.3</td><td>195.9</td><td>44.2</td><td>67.0</td><td>55.1</td></tr>
<tr><td>Adjusted rate</td><td>115.8</td><td>153.3</td><td>132.4</td><td>27.9</td><td>51.6</td><td>38.3</td></tr>
<tr><td>Lower 95% Limit</td><td>102.3</td><td>135.3</td><td>121.4</td><td>21.3</td><td>41.4</td><td>32.4</td></tr>
<tr><td>Upper 95% Limit</td><td>130.9</td><td>173.2</td><td>144.3</td><td>36.1</td><td>63.8</td><td>45.1</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>253.4</td><td>246.2</td><td>249.9</td><td>111.2</td><td>143.8</td><td>126.8</td></tr>
<tr><td>Adjusted rate</td><td>148.2</td><td>188.4</td><td>165.8</td><td>64.1</td><td>111.5</td><td>84.4</td></tr>
<tr><td>Lower 95% Limit</td><td>132.9</td><td>168.4</td><td>153.5</td><td>54.3</td><td>96.2</td><td>75.7</td></tr>
<tr><td>Upper 95% Limit</td><td>164.9</td><td>210.2</td><td>178.9</td><td>75.4</td><td>128.8</td><td>94.0</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2014"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2014</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>179.1</td><td>165.9</td><td>172.8</td><td>75.1</td><td>93.8</td><td>84.1</td></tr>
<tr><td>Adjusted rate</td><td>106.6</td><td>125.3</td><td>115.3</td><td>44.4</td><td>70.4</td><td>56.1</td></tr>
<tr><td>Lower 95% Limit</td><td>93.6</td><td>109.2</td><td>105.0</td><td>36.3</td><td>58.5</td><td>49.0</td></tr>
<tr><td>Upper 95% Limit</td><td>121.2</td><td>143.3</td><td>126.4</td><td>54.1</td><td>84.1</td><td>64.0</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>217.7</td><td>201.2</td><td>209.8</td><td>130.9</td><td>165.2</td><td>147.3</td></tr>
<tr><td>Adjusted rate</td><td>126.5</td><td>151.7</td><td>137.4</td><td>72.3</td><td>124.0</td><td>95.2</td></tr>
<tr><td>Lower 95% Limit</td><td>112.4</td><td>134.0</td><td>126.3</td><td>62.1</td><td>108.1</td><td>86.1</td></tr>
<tr><td>Upper 95% Limit</td><td>142.1</td><td>171.3</td><td>149.4</td><td>84.0</td><td>141.8</td><td>105.1</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2015"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2015</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>175.3</td><td>171.5</td><td>173.5</td><td>68.8</td><td>83.1</td><td>75.6</td></tr>
<tr><td>Adjusted rate</td><td>102.4</td><td>126.4</td><td>113.8</td><td>40.4</td><td>63.1</td><td>51.2</td></tr>
<tr><td>Lower 95% Limit</td><td>89.8</td><td>110.5</td><td>103.8</td><td>32.7</td><td>51.8</td><td>44.4</td></tr>
<tr><td>Upper 95% Limit</td><td>116.6</td><td>144.2</td><td>124.7</td><td>49.7</td><td>76.3</td><td>58.8</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>219.4</td><td>199.9</td><td>210.0</td><td>108.0</td><td>126.5</td><td>116.9</td></tr>
<tr><td>Adjusted rate</td><td>124.0</td><td>147.4</td><td>135.5</td><td>60.6</td><td>95.3</td><td>76.7</td></tr>
<tr><td>Lower 95% Limit</td><td>110.3</td><td>130.1</td><td>124.6</td><td>51.3</td><td>81.3</td><td>68.4</td></tr>
<tr><td>Upper 95% Limit</td><td>139.2</td><td>166.4</td><td>147.2</td><td>71.5</td><td>111.0</td><td>85.7</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2016"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2016</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>207.3</td><td>194.9</td><td>201.4</td><td>65.2</td><td>91.1</td><td>77.6</td></tr>
<tr><td>Adjusted rate</td><td>122.3</td><td>141.2</td><td>131.9</td><td>38.3</td><td>67.3</td><td>51.8</td></tr>
<tr><td>Lower 95% Limit</td><td>108.3</td><td>124.5</td><td>121.0</td><td>30.7</td><td>55.8</td><td>45.0</td></tr>
<tr><td>Upper 95% Limit</td><td>137.9</td><td>159.7</td><td>143.5</td><td>47.4</td><td>80.7</td><td>59.4</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>269.7</td><td>246.4</td><td>258.6</td><td>129.7</td><td>186.7</td><td>157.0</td></tr>
<tr><td>Adjusted rate</td><td>154.4</td><td>178.7</td><td>166.2</td><td>70.6</td><td>136.1</td><td>100.5</td></tr>
<tr><td>Lower 95% Limit</td><td>138.8</td><td>159.8</td><td>154.0</td><td>60.6</td><td>119.6</td><td>91.2</td></tr>
<tr><td>Upper 95% Limit</td><td>171.5</td><td>199.4</td><td>179.1</td><td>82.1</td><td>154.4</td><td>110.7</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2017"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2017</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>196.7</td><td>191.5</td><td>194.2</td><td>89.8</td><td>109.5</td><td>99.2</td></tr>
<tr><td>Adjusted rate</td><td>113.5</td><td>137.8</td><td>124.4</td><td>52.8</td><td>77.9</td><td>64.3</td></tr>
<tr><td>Lower 95% Limit</td><td>100.2</td><td>121.3</td><td>113.9</td><td>43.9</td><td>65.7</td><td>56.8</td></tr>
<tr><td>Upper 95% Limit</td><td>128.2</td><td>156.1</td><td>135.6</td><td>63.2</td><td>91.9</td><td>72.5</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>238.5</td><td>225.0</td><td>232.0</td><td>146.6</td><td>188.5</td><td>166.7</td></tr>
<tr><td>Adjusted rate</td><td>134.1</td><td>161.5</td><td>146.7</td><td>81.2</td><td>134.6</td><td>104.9</td></tr>
<tr><td>Lower 95% Limit</td><td>119.8</td><td>143.7</td><td>135.4</td><td>70.3</td><td>118.4</td><td>95.5</td></tr>
<tr><td>Upper 95% Limit</td><td>149.9</td><td>181.2</td><td>158.8</td><td>93.5</td><td>152.6</td><td>115.2</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2018"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2018</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>189.5</td><td>202.9</td><td>195.9</td><td>72.5</td><td>112.2</td><td>91.6</td></tr>
<tr><td>Adjusted rate</td><td>107.7</td><td>143.1</td><td>124.2</td><td>40.9</td><td>80.0</td><td>58.3</td></tr>
<tr><td>Lower 95% Limit</td><td>94.8</td><td>126.4</td><td>113.8</td><td>33.3</td><td>67.6</td><td>51.3</td></tr>
<tr><td>Upper 95% Limit</td><td>122.0</td><td>161.5</td><td>135.5</td><td>50.0</td><td>94.1</td><td>66.1</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>242.9</td><td>243.1</td><td>243.0</td><td>146.4</td><td>199.9</td><td>172.1</td></tr>
<tr><td>Adjusted rate</td><td>134.9</td><td>172.0</td><td>152.4</td><td>77.8</td><td>142.3</td><td>106.8</td></tr>
<tr><td>Lower 95% Limit</td><td>120.6</td><td>153.6</td><td>140.9</td><td>67.5</td><td>125.6</td><td>97.4</td></tr>
<tr><td>Upper 95% Limit</td><td>150.7</td><td>192.1</td><td>164.7</td><td>89.6</td><td>160.7</td><td>117.1</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2019"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2019</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>217.9</td><td>224.7</td><td>221.2</td><td>103.2</td><td>118.7</td><td>110.6</td></tr>
<tr><td>Adjusted rate</td><td>119.1</td><td>152.2</td><td>135.1</td><td>55.4</td><td>82.5</td><td>68.4</td></tr>
<tr><td>Lower 95% Limit</td><td>105.9</td><td>135.4</td><td>124.5</td><td>46.7</td><td>70.0</td><td>60.8</td></tr>
<tr><td>Upper 95% Limit</td><td>133.7</td><td>170.8</td><td>146.5</td><td>65.5</td><td>96.8</td><td>76.7</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>270.5</td><td>268.5</td><td>269.6</td><td>188.5</td><td>201.0</td><td>194.5</td></tr>
<tr><td>Adjusted rate</td><td>144.1</td><td>183.1</td><td>162.5</td><td>97.6</td><td>140.5</td><td>118.1</td></tr>
<tr><td>Lower 95% Limit</td><td>129.8</td><td>164.6</td><td>151.0</td><td>86.1</td><td>124.1</td><td>108.2</td></tr>
<tr><td>Upper 95% Limit</td><td>159.9</td><td>203.4</td><td>174.8</td><td>110.6</td><td>158.8</td><td>128.8</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2020"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2020</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>196.5</td><td>203.5</td><td>199.9</td><td>85.3</td><td>122.9</td><td>103.3</td></tr>
<tr><td>Adjusted rate</td><td>110.1</td><td>139.4</td><td>124.3</td><td>45.5</td><td>84.7</td><td>63.0</td></tr>
<tr><td>Lower 95% Limit</td><td>97.2</td><td>123.1</td><td>114.0</td><td>37.7</td><td>72.2</td><td>55.8</td></tr>
<tr><td>Upper 95% Limit</td><td>124.6</td><td>157.4</td><td>135.4</td><td>54.9</td><td>99.1</td><td>70.9</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>248.3</td><td>248.0</td><td>248.1</td><td>178.7</td><td>211.0</td><td>194.2</td></tr>
<tr><td>Adjusted rate</td><td>136.2</td><td>169.3</td><td>152.3</td><td>91.1</td><td>146.6</td><td>116.8</td></tr>
<tr><td>Lower 95% Limit</td><td>121.9</td><td>151.4</td><td>140.9</td><td>80.1</td><td>129.9</td><td>107.0</td></tr>
<tr><td>Upper 95% Limit</td><td>152.1</td><td>189.0</td><td>164.5</td><td>103.7</td><td>165.2</td><td>127.3</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2021"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2021</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>179.2</td><td>196.5</td><td>187.5</td><td>60.6</td><td>82.7</td><td>71.2</td></tr>
<tr><td>Adjusted rate</td><td>98.0</td><td>133.0</td><td>113.6</td><td>34.0</td><td>57.2</td><td>44.8</td></tr>
<tr><td>Lower 95% Limit</td><td>86.0</td><td>117.3</td><td>103.9</td><td>27.0</td><td>46.9</td><td>38.6</td></tr>
<tr><td>Upper 95% Limit</td><td>111.5</td><td>150.6</td><td>124.1</td><td>42.6</td><td>69.2</td><td>51.7</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>243.2</td><td>246.8</td><td>244.9</td><td>151.2</td><td>181.0</td><td>165.5</td></tr>
<tr><td>Adjusted rate</td><td>126.9</td><td>166.9</td><td>144.7</td><td>76.5</td><td>122.0</td><td>97.3</td></tr>
<tr><td>Lower 95% Limit</td><td>113.6</td><td>149.2</td><td>133.9</td><td>66.4</td><td>107.0</td><td>88.5</td></tr>
<tr><td>Upper 95% Limit</td><td>141.8</td><td>186.3</td><td>156.3</td><td>88.0</td><td>138.7</td><td>106.8</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2022"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2022</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>194.7</td><td>209.0</td><td>201.5</td><td>71.5</td><td>99.7</td><td>85.0</td></tr>
<tr><td>Adjusted rate</td><td>106.2</td><td>135.6</td><td>119.6</td><td>38.8</td><td>65.5</td><td>50.9</td></tr>
<tr><td>Lower 95% Limit</td><td>93.6</td><td>120.0</td><td>109.7</td><td>31.5</td><td>54.7</td><td>44.5</td></tr>
<tr><td>Upper 95% Limit</td><td>120.2</td><td>152.9</td><td>130.2</td><td>47.7</td><td>78.0</td><td>58.1</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>261.4</td><td>283.6</td><td>272.0</td><td>174.9</td><td>231.1</td><td>201.9</td></tr>
<tr><td>Adjusted rate</td><td>136.0</td><td>187.1</td><td>158.7</td><td>87.9</td><td>153.9</td><td>116.5</td></tr>
<tr><td>Lower 95% Limit</td><td>122.1</td><td>168.6</td><td>147.4</td><td>77.2</td><td>137.1</td><td>106.9</td></tr>
<tr><td>Upper 95% Limit</td><td>151.3</td><td>207.4</td><td>170.8</td><td>100.2</td><td>172.6</td><td>126.8</td></tr>
</tbody></table></div>
<div class="bnr-table-wrapper bnr-year-table" data-bnr-year="2023"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Both</th>
  <th>Female</th><th>Male</th><th>Both</th>
</tr>
</thead>
<tbody><tr><td>2023</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Does Event Rate include DCOs?</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Without DCO</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>212.3</td><td>230.5</td><td>221.0</td><td>71.4</td><td>104.2</td><td>87.1</td></tr>
<tr><td>Adjusted rate</td><td>111.9</td><td>154.0</td><td>130.4</td><td>38.4</td><td>68.0</td><td>52.3</td></tr>
<tr><td>Lower 95% Limit</td><td>99.2</td><td>137.0</td><td>120.0</td><td>31.1</td><td>57.0</td><td>45.8</td></tr>
<tr><td>Upper 95% Limit</td><td>126.1</td><td>172.7</td><td>141.5</td><td>47.3</td><td>80.7</td><td>59.6</td></tr>
<tr><td>DCO added</td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Crude rate</td><td>276.9</td><td>292.5</td><td>284.4</td><td>181.7</td><td>219.4</td><td>199.8</td></tr>
<tr><td>Adjusted rate</td><td>141.0</td><td>197.9</td><td>166.5</td><td>89.9</td><td>144.8</td><td>115.6</td></tr>
<tr><td>Lower 95% Limit</td><td>126.9</td><td>178.4</td><td>154.8</td><td>79.0</td><td>128.5</td><td>106.0</td></tr>
<tr><td>Upper 95% Limit</td><td>156.5</td><td>219.0</td><td>178.9</td><td>102.3</td><td>162.8</td><td>125.9</td></tr>
</tbody></table></div>
</div>

[Download Data](../downloads/data/bnr-cvd-2023-table5.xlsx){ .md-button .btn-right}
<br/><br/>

---

## **Table 6.** CVD Incidence Rate Ratios (2010 to 2023) for Hospital Events   
### Incidence Rate Ratios, Comparing Event Type, Sex, Time Periods.

<div class="bnr-table-wrapper">
  <table class="bnr-table">
    <thead>
      <tr>
        <th></th>
        <th>IRR</th>
        <th>Lower 95% Limit</th>
        <th>Upper 95% Limit</th>
      </tr>
    </thead>
    <tbody>
      <tr><td><strong>Incidence Rate Comparison † ‡</strong></td><td></td><td></td><td></td></tr>

      <tr><td>Stroke (vs. AMI)</td><td>2.34</td><td>2.27</td><td>2.41</td></tr>
      <tr><td>CVD in Men (vs. Women)</td><td>1.39</td><td>1.33</td><td>1.44</td></tr>

      <tr><td>2012–2013 (vs. 2010–11)</td><td>1.32</td><td>1.17</td><td>1.48</td></tr>
      <tr><td>2014–2015</td><td>1.67</td><td>1.49</td><td>1.87</td></tr>
      <tr><td>2016–2017</td><td>1.81</td><td>1.62</td><td>2.02</td></tr>
      <tr><td>2018–2019</td><td>1.97</td><td>1.77</td><td>2.20</td></tr>
      <tr><td>2020–2021</td><td>1.67</td><td>1.50</td><td>1.87</td></tr>
      <tr><td>2022–2023</td><td>1.61</td><td>1.43</td><td>1.80</td></tr>

      <tr><td>2012–2013</td><td>1.12</td><td>1.05</td><td>1.20</td></tr>
      <tr><td>2014–2015</td><td>1.12</td><td>1.04</td><td>1.19</td></tr>
      <tr><td>2016–2017</td><td>1.25</td><td>1.17</td><td>1.33</td></tr>
      <tr><td>2018–2019</td><td>1.26</td><td>1.18</td><td>1.35</td></tr>
      <tr><td>2020–2021</td><td>1.16</td><td>1.08</td><td>1.24</td></tr>
      <tr><td>2022–2023</td><td>1.22</td><td>1.14</td><td>1.30</td></tr>

      <tr><td colspan="4"><em>Prepared by Ian Hambleton, 2025-11-19</em></td></tr>
      <tr><td colspan="4"><em>† IRR = Incidence Rate Ratio</em></td></tr>
      <tr><td colspan="4"><em>‡ Time periods compared with 2010–2011</em></td></tr>
    </tbody>
  </table>
</div>

[Download Data](../downloads/data/bnr-cvd-2023-table6.xlsx){ .md-button .btn-right}
<br/><br/>

--- 

## **Table 7.** CVD In-Hospital Fatality Percentage (2010 to 2023)   
### Comparing In-Hospital Deaths by Event Type, Sex, Time Periods.

<div class="bnr-table-wrapper"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">Two-year interval</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
  <th colspan="3">Total</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Total</th>
  <th>Female</th><th>Male</th><th>Total</th>
  <th>Female</th><th>Male</th><th>Total</th>
</tr>
</thead>
<tbody>
<tr><td>2022-2023</td><td>20.6</td><td>21.5</td><td>21.0</td><td>26.7</td><td>18.8</td><td>22.8</td><td>23.6</td><td>20.2</td><td>21.9</td></tr>
<tr><td>2020-2021</td><td>33.8</td><td>26.2</td><td>30.0</td><td>28.5</td><td>24.8</td><td>26.7</td><td>31.1</td><td>25.5</td><td>28.3</td></tr>
<tr><td>2018-2019</td><td>35.7</td><td>29.0</td><td>32.4</td><td>26.8</td><td>22.8</td><td>24.8</td><td>31.3</td><td>25.9</td><td>28.6</td></tr>
<tr><td>2016-2017</td><td>35.1</td><td>31.1</td><td>33.1</td><td>20.4</td><td>18.2</td><td>19.3</td><td>27.7</td><td>24.6</td><td>26.2</td></tr>
<tr><td>2014-2015</td><td>28.7</td><td>28.9</td><td>28.8</td><td>28.7</td><td>23.3</td><td>26.0</td><td>28.7</td><td>26.1</td><td>27.4</td></tr>
<tr><td>2012-2013</td><td>30.8</td><td>33.0</td><td>31.9</td><td>25.0</td><td>15.0</td><td>20.0</td><td>27.9</td><td>24.0</td><td>26.0</td></tr>
<tr><td>2010-2011</td><td>30.0</td><td>26.4</td><td>28.2</td><td>19.0</td><td>10.7</td><td>14.9</td><td>24.5</td><td>18.5</td><td>21.5</td></tr>
<tr><td>Total</td><td>30.7</td><td>28.0</td><td>29.3</td><td>25.0</td><td>19.1</td><td>22.1</td><td>27.8</td><td>23.6</td><td>25.7</td></tr>
</tbody></table></div>

[Download Data](../downloads/data/bnr-cvd-2023-table7.xlsx){ .md-button .btn-right}
<br/><br/>

---

## **Table 8.** CVD Typical (Median) In-Hospital Length of Stay (2010 to 2023)   
### Comparing in-Hospital Length of Stay by Event Type, Sex, Time Periods.

<div class="bnr-table-wrapper"><table class="bnr-table">
<thead>
<tr>
  <th rowspan="3">CVD Event Year</th>
  <th colspan="3">Stroke</th>
  <th colspan="3">AMI</th>
  <th colspan="3">Total</th>
</tr>
<tr>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
  <th colspan="3">Patient sex</th>
</tr>
<tr>
  <th>Female</th><th>Male</th><th>Total</th>
  <th>Female</th><th>Male</th><th>Total</th>
  <th>Female</th><th>Male</th><th>Total</th>
</tr>
</thead>
<tbody>

<tr><td>CVD Event Year</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>2023</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>9</td><td>11</td><td>10</td><td>7</td><td>6</td><td>7</td><td>9</td><td>8</td><td>8</td></tr>
<tr><td>25th percentile</td><td>4</td><td>4</td><td>4</td><td>5</td><td>5</td><td>5</td><td>4</td><td>5</td><td>5</td></tr>
<tr><td>75th percentile</td><td>20</td><td>20</td><td>20</td><td>9</td><td>10</td><td>9</td><td>15</td><td>15</td><td>15</td></tr>
<tr><td>2022</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>11</td><td>9</td><td>10</td><td>8</td><td>6</td><td>6</td><td>9</td><td>7</td><td>8</td></tr>
<tr><td>25th percentile</td><td>3</td><td>3</td><td>3</td><td>6</td><td>4</td><td>5</td><td>5</td><td>4</td><td>4</td></tr>
<tr><td>75th percentile</td><td>21</td><td>19</td><td>19</td><td>10</td><td>8</td><td>9</td><td>17</td><td>15</td><td>16</td></tr>
<tr><td>2021</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>7</td><td>10</td><td>8</td><td>6</td><td>5</td><td>6</td><td>7</td><td>7</td><td>7</td></tr>
<tr><td>25th percentile</td><td>3</td><td>4</td><td>3</td><td>5</td><td>4</td><td>5</td><td>3</td><td>4</td><td>4</td></tr>
<tr><td>75th percentile</td><td>19</td><td>20</td><td>19</td><td>9</td><td>7</td><td>8</td><td>15</td><td>15</td><td>15</td></tr>
<tr><td>2020</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>6</td><td>7</td><td>7</td><td>6</td><td>6</td><td>6</td><td>6</td><td>7</td><td>6</td></tr>
<tr><td>25th percentile</td><td>2</td><td>3</td><td>2</td><td>4</td><td>4</td><td>4</td><td>3</td><td>4</td><td>3</td></tr>
<tr><td>75th percentile</td><td>12</td><td>17</td><td>15</td><td>8</td><td>8</td><td>8</td><td>10</td><td>14</td><td>11</td></tr>
<tr><td>2019</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>8</td><td>9</td><td>9</td><td>7</td><td>6</td><td>6</td><td>7</td><td>7</td><td>7</td></tr>
<tr><td>25th percentile</td><td>3</td><td>4</td><td>4</td><td>5</td><td>4</td><td>4</td><td>4</td><td>4</td><td>4</td></tr>
<tr><td>75th percentile</td><td>18</td><td>21</td><td>20</td><td>9</td><td>8</td><td>9</td><td>14</td><td>14</td><td>14</td></tr>
<tr><td>2018</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>6</td><td>7</td><td>7</td><td>7</td><td>6</td><td>6</td><td>7</td><td>6</td><td>6</td></tr>
<tr><td>25th percentile</td><td>1</td><td>3</td><td>2</td><td>5</td><td>4</td><td>5</td><td>2</td><td>4</td><td>3</td></tr>
<tr><td>75th percentile</td><td>16</td><td>19</td><td>18</td><td>10</td><td>8</td><td>9</td><td>12</td><td>14</td><td>13</td></tr>
<tr><td>2017</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>6</td><td>9</td><td>7</td><td>7</td><td>6</td><td>6</td><td>6</td><td>7</td><td>7</td></tr>
<tr><td>25th percentile</td><td>1</td><td>3</td><td>2</td><td>5</td><td>4</td><td>4</td><td>3</td><td>4</td><td>3</td></tr>
<tr><td>75th percentile</td><td>13</td><td>20</td><td>16</td><td>10</td><td>9</td><td>10</td><td>12</td><td>15</td><td>13</td></tr>
<tr><td>2016</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>6</td><td>5</td><td>5</td><td>6</td><td>6</td><td>6</td><td>6</td><td>6</td><td>6</td></tr>
<tr><td>25th percentile</td><td>1</td><td>1</td><td>1</td><td>4</td><td>5</td><td>5</td><td>2</td><td>3</td><td>3</td></tr>
<tr><td>75th percentile</td><td>16</td><td>11</td><td>13</td><td>9</td><td>8</td><td>8</td><td>13</td><td>8</td><td>10</td></tr>
<tr><td>2015</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>5</td><td>6</td><td>5</td><td>6</td><td>6</td><td>6</td><td>5</td><td>6</td><td>6</td></tr>
<tr><td>25th percentile</td><td>2</td><td>2</td><td>2</td><td>4</td><td>4</td><td>4</td><td>3</td><td>3</td><td>3</td></tr>
<tr><td>75th percentile</td><td>11</td><td>14</td><td>12</td><td>8</td><td>8</td><td>8</td><td>10</td><td>11</td><td>10</td></tr>
<tr><td>2014</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>5</td><td>6</td><td>6</td><td>5</td><td>5</td><td>5</td><td>5</td><td>6</td><td>5</td></tr>
<tr><td>25th percentile</td><td>2</td><td>2</td><td>2</td><td>4</td><td>4</td><td>4</td><td>3</td><td>3</td><td>3</td></tr>
<tr><td>75th percentile</td><td>14</td><td>16</td><td>14</td><td>7</td><td>7</td><td>7</td><td>12</td><td>12</td><td>12</td></tr>
<tr><td>2013</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>8</td><td>7</td><td>7</td><td>7</td><td>6</td><td>6</td><td>7</td><td>6</td><td>7</td></tr>
<tr><td>25th percentile</td><td>4</td><td>3</td><td>3</td><td>6</td><td>5</td><td>5</td><td>4</td><td>3</td><td>4</td></tr>
<tr><td>75th percentile</td><td>15</td><td>14</td><td>15</td><td>12</td><td>8</td><td>10</td><td>14</td><td>11</td><td>13</td></tr>
<tr><td>2012</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>7</td><td>6</td><td>7</td><td>7</td><td>6</td><td>6</td><td>7</td><td>6</td><td>6</td></tr>
<tr><td>25th percentile</td><td>2</td><td>2</td><td>2</td><td>4</td><td>5</td><td>4</td><td>3</td><td>4</td><td>3</td></tr>
<tr><td>75th percentile</td><td>14</td><td>11</td><td>12</td><td>10</td><td>8</td><td>9</td><td>11</td><td>10</td><td>10</td></tr>
<tr><td>2011</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>4</td><td>5</td><td>5</td><td>6</td><td>5</td><td>6</td><td>5</td><td>5</td><td>5</td></tr>
<tr><td>25th percentile</td><td>1</td><td>2</td><td>1</td><td>5</td><td>5</td><td>5</td><td>2</td><td>3</td><td>2</td></tr>
<tr><td>75th percentile</td><td>9</td><td>12</td><td>11</td><td>11</td><td>8</td><td>9</td><td>9</td><td>11</td><td>11</td></tr>
<tr><td>2010</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>3</td><td>5</td><td>3</td><td>7</td><td>7</td><td>7</td><td>4</td><td>6</td><td>5</td></tr>
<tr><td>25th percentile</td><td>1</td><td>1</td><td>1</td><td>5</td><td>5</td><td>5</td><td>1</td><td>1</td><td>1</td></tr>
<tr><td>75th percentile</td><td>8</td><td>11</td><td>10</td><td>10</td><td>9</td><td>9</td><td>9</td><td>10</td><td>10</td></tr>
<tr><td>Total</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr>
<tr><td>Median</td><td>6</td><td>7</td><td>7</td><td>6</td><td>6</td><td>6</td><td>6</td><td>6</td><td>6</td></tr>
<tr><td>25th percentile</td><td>2</td><td>2</td><td>2</td><td>5</td><td>4</td><td>5</td><td>3</td><td>4</td><td>3</td></tr>
<tr><td>75th percentile</td><td>15</td><td>17</td><td>16</td><td>9</td><td>8</td><td>9</td><td>12</td><td>12</td><td>12</td></tr>
</tbody></table></div>

[Download Data](../downloads/data/bnr-cvd-2023-table8.xlsx){ .md-button .btn-right}
<br/><br/>

---

<!-- JavaScript to control year choice in Table 2 -->
<script>
  (function () {
    document.querySelectorAll('.bnr-year-block').forEach(function (block) {
      var select = block.querySelector('.bnr-year-select');
      if (!select) return;

      function updateTables() {
        var year = select.value;
        block.querySelectorAll('.bnr-year-table').forEach(function (wrapper) {
          if (wrapper.getAttribute('data-bnr-year') === year) {
            wrapper.style.display = 'block';
          } else {
            wrapper.style.display = 'none';
          }
        });
      }

      // On change, switch visible table
      select.addEventListener('change', updateTables);

      // Initialise correct table on load
      updateTables();
    });
  })();
</script>

