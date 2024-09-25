# slackbuild-hyprland


Aqui tengo los slackbuilds de hyprland. Alghnos estan en SBo y otros no.

Las dependencias que no estan agregadas estan en slackbuilds-sway.


<b>NOTA:</b> 

Para poder montar y desmontar unidades extraibles, como USBs, se debe modificar el archivo de arranque de hyprland y cambiar la línea Exec para que quede:

Exec=dbus-launch --sh-syntax --exit-with-session Hyprland

Probé udiskie, pero no permite desmontar o extraer las unidades como usuario no-root.

<b>NOTA 2</b>

<b>En caso de usar init 3,</b> para habiltar pipewire,  se deben realizar dos pasos:

1-  Como root, /usr/sbin/pipewire-enable.sh

2- Luego en el archivo de inicialización de Hyprland, antes de la línea para iniciarlo, se agrega:

/usr/bin/daemon -rB --pidfiles=~/.run --name=pipewire /usr/bin/pipewire

/usr/bin/daemon -rB --pidfiles=~/.run --name=pipewire-pulse /usr/bin/pipewire-pulse

/usr/bin/daemon -rB --pidfiles=~/.run --name=wireplumber /usr/bin/wireplumber

<b>En caso de usar init 4, usando sddm.</b>

Como root, /usr/sbin/pipewire-enable.sh y se deben añadir estas tres líneas a /usr/share/sddm/scripts/wayland-session.

En mi caso quedó:

.....

esac

# EXPERIMENTAL

# Supuestamente cargaría pipewire al arrancar con sddm

#

/usr/bin/daemon -rB --pidfiles=~/.run --name=pipewire /usr/bin/pipewire 

/usr/bin/daemon -rB --pidfiles=~/.run --name=pipewire-pulse /usr/bin/pipewire-pulse

/usr/bin/daemon -rB --pidfiles=~/.run --name=wireplumber /usr/bin/wireplumber


# Restore user shell setting that may have been clobbered by setting environment

export SHELL=$SDDM_USER_SHE

......


Javier Aragones (javaragones at gmail at com)
