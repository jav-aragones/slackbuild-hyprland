# slackbuild-hyprland


Aqui tengo los slackbuilds de hyprland. Alghnos estan en SBo y otros no.

Las dependencias que no estan agregadas estan en slackbuilds-swayi.

Incluí udisksie que automonta unidades extraibles como USBs.


<b>NOTA:</b>  En caso de no instalar udiskie, se debe modificar el archivo /usr/share/wayland-sessions/hyprland.desktop,

hay que cambiar la línea Exec para que quede:


Exec=dbus-launch --sh-syntax --exit-with-session Hyprland


Esto reemplazael uso de udiskie ya que permite poder montar unidades extraibles como usuario no root.


Javier Aragones (javaragones at gmail at com)
