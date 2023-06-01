<!-- markdownlint-disable MD033 MD041 -->
{::nomarkdown}<div class="table">{:/}

<table>
  <thead>
    <tr>
      {% if include.modes[0].type %}
      <th>Type (name)</th>
      {% else %}
      <th>Mode (name)</th>
      {% endif %}
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    {% for mode in include.modes %}
    <tr>
      <td>
        {% assign code = mode.type if mode.type else mode.mode %}
        <a name="{{ code }}">
          <code>{{ code }}</code>
          <br/>
          {{ mode.name }}
        </a>
      </td>
      <td>{{ mode.description | markdownify }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>

{::nomarkdown}</div>{:/}
