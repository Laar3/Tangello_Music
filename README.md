# Tangello_Music
Welcome to Tangello music, a graphical mpd client written in rust using egui.

Currently in early development and any help is welcome. Even if you just have suggestions for new features (although basic functionality is still being worked on at the moment) please open an issue or shoot me an email at `laar@tutanota.com`.
![image](https://user-images.githubusercontent.com/77225642/173051231-acbaf78c-6398-434a-8673-e9ed7c67a28e.png)



# Install instructions:
Dependancies:
```
rust/cargo
mpd
```
1: Set up mpd and start it, the following is a good basic config file if you are running linux 
https://raw.githubusercontent.com/LukeSmithxyz/voidrice/master/.config/mpd/mpd.conf
Put that file into `~/.config/mpd/mpd.conf` then start up mpd.
2: Git clone the repo and cd into it.
```
git clone https://github.com/Laar3/Tangello_Music/
cd Tangello_Music
```
3: Compile with cargo.
For developement simply run `cargo run` 
For building the final product with all optimisations enabled, run.
`cargo build --release`, the binary will then appear in the projects target directory under release (`target/release/tangello_music`)

4: Run the binary with `./tangello_music` or copying it into your path.

# Helpful hints:
Currently tangello will only find musics album art when that song is exactly 2 directories deep in your music folder, this is an issue that is being worked on.
An example is a song must be in `music/foo/bar/song.flac` for its album art to be picked up.
In order to sort your music if your running linux cd into your music directory and run the sorter script in the repo, if you want to revert the changes, again cd into the music directory and run `sorter unsort`, this will bring your songs into the top level of the music dir.
Example usage for the sorting script:
```
cd Music
../Tangello_Music/sorter 
```
Please note that the scipt requires ffmpeg to be installed.

Because of a limitation in mpd-rs that i havnt been able to figure out yet album art requires you to specify the music folder in the settings of tangello, not just in your mpd config file like normal. This is not a super high priority to be fixed as im not sure how to go about it but its on my radar.