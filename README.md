# CODE-RUNNER
#MUSIC-PLAYER
#HTML-FILE
<div class="player" data-player data-playlist="boxer" data-track="0">

    <div class="player__content">

        <div class="player__artist has-fade-in" data-player-album-artist>Tronix</div>
        <div class="player__album has-fade-in" data-player-album-name>Sonar</div>
        <div class="player__track has-fade-in" data-player-album-song>Mosh Pit</div>

        <div class="album album--boxer" data-album>
            <div class="album__cover"></div>
            <div class="vinyl">
                <div class="vinyl__shadow"></div>
                <div class="vinyl__circle">
                    <div class="vinyl__center"></div>
                </div> 
            </div>
            <!-- /.vinyl -->
        </div>
        <!-- /.album -->

        <div class="player__controls has-fade-in">
            <div class="player__controls-item player__controls-item--prev" data-player-prev></div>
            <div class="player__controls-item player__controls-item--play" data-player-play>
                <div class="rectangle"></div>
                <div class="triangle"></div>
            </div>
            <div class="player__controls-item player__controls-item--next" data-player-next></div>
        </div>
        <!-- /.player__controls -->

        <audio preload>Your browser does not support HTML5 Audio!</audio>

    </div>
    <!-- /.player__content -->

</div>
<!-- /.player -->

<div class="player" data-player data-playlist="billionaires2014Compilation" data-track="0">

    <div class="player__content">

        <div class="player__artist has-fade-in" data-player-album-artist>Tronix</div>
        <div class="player__album has-fade-in" data-player-album-name>Sonar</div>
        <div class="player__track has-fade-in" data-player-album-song>Mosh Pit</div>

        <div class="album album--billionaires-2014-compilation" data-album>
            <div class="album__cover"></div>
            <div class="vinyl">
                <div class="vinyl__shadow"></div>
                <div class="vinyl__circle">
                    <div class="vinyl__center"></div>
                </div> 
            </div>
            <!-- /.vinyl -->
        </div>
        <!-- /.album -->

        <div class="player__controls has-fade-in">
            <div class="player__controls-item player__controls-item--prev" data-player-prev></div>
            <div class="player__controls-item player__controls-item--play" data-player-play>
                <div class="rectangle"></div>
                <div class="triangle"></div>
            </div>
            <div class="player__controls-item player__controls-item--next" data-player-next></div>
        </div>
        <!-- /.player__controls -->

        <audio preload>Your browser does not support HTML5 Audio!</audio>

    </div>
    <!-- /.player__content -->

</div>
<!-- /.player -->

<div class="player" data-player data-playlist="projectMayhem" data-track="0">

    <div class="player__content">

        <div class="player__artist has-fade-in" data-player-album-artist>Tronix</div>
        <div class="player__album has-fade-in" data-player-album-name>Sonar</div>
        <div class="player__track has-fade-in" data-player-album-song>Mosh Pit</div>

        <div class="album album--project-mayhem" data-album>
            <div class="album__cover"></div>
            <div class="vinyl">
                <div class="vinyl__shadow"></div>
                <div class="vinyl__circle">
                    <div class="vinyl__center"></div>
                </div> 
            </div>
            <!-- /.vinyl -->
        </div>
        <!-- /.album -->

        <div class="player__controls has-fade-in">
            <div class="player__controls-item player__controls-item--prev" data-player-prev></div>
            <div class="player__controls-item player__controls-item--play" data-player-play>
                <div class="rectangle"></div>
                <div class="triangle"></div>
            </div>
            <div class="player__controls-item player__controls-item--next" data-player-next></div>
        </div>
        <!-- /.player__controls -->

        <audio preload>Your browser does not support HTML5 Audio!</audio>

    </div>
    <!-- /.player__content -->

</div>
<!-- /.player -->
 
 CSS-FILE
 @import 'bourbon';

@import url(https://fonts.googleapis.com/css?family=Raleway:400,300,500);

$color-black: #000;
$color-gray: #5e6062;
$color-white: #fff;
$color-yellow: #f0f39c;
$color-yellow-light: #fff99e;

$transition-time: 250ms;
$transition-method: ease-in-out;

$album-size: 310px;
$vinyl-offset: 20px;
$vinyl-size: $album-size - $vinyl-offset;
$vinyl-center-size: 146px;

html {
    background-color: $color-yellow;
    box-sizing: border-box;
}
// html

*, 
*:before, 
*:after {
    box-sizing: inherit;
    line-height: inherit;
}
// *, *:before, *:after

.player {
    @include transition(all $transition-time $transition-method);
    color: $color-gray;
    font-family: 'Raleway', sans-serif;
    height: $album-size;
    line-height: 1.2;
    margin: 50px auto;
    position: relative;
    width: $album-size;

    &:after {
        @include transform(rotate(-2deg));
        @include transition(all $transition-time $transition-method);
        background: #777;
        bottom: 12px;
        box-shadow: 0 15px 23px rgba($color-black, 0.3);
        content: '';
        height: 10px;
        left: 2%;
        opacity: 0;
        padding-left: 5%;
        position: absolute;
        width: 96%;
        z-index: 5;
    }
    // &:after

    .player__content {
        background-color: $color-white;
        height: 100%;
        padding: 100px 0 0 20px;
        position: relative;
        text-align: right;
        width: 100%;
        z-index: 10;
    }
    // .player__content

    .player__artist {
        font-size: 24px;
        font-weight: 500;
        margin-bottom: 10px;
        width: 200px;
    }
    // .player__artist

    .player__album {
        font-size: 20px;
        font-weight: 300;
        margin-bottom: 30px;
        width: 200px;
    }
    // .player__album

    .player__track {
        font-size: 16px;
        font-weight: 300;
        margin-bottom: 30px;
        width: 200px;

        &:before,
        &:after {
            content: '"';
            font-size: 22px;
            vertical-align: middle;
        }
        // &:before, &:after

    }
    // .player__track

}
// .player

.player--open {
    border-radius: 2px;
    height: 370px;
    position: relative;
    width: 460px;

    &:after {
        opacity: 1;
    }
    // &:after

}
// .player--open

.player__controls {
    $size: 26px;
    $speed: 0.3s;
    bottom: 45px;
    left: 0;
    position: absolute;
    text-align: center;
    white-space: nowrap;
    width: 250px;
    
    &-item {
        @include user-select(none);
        cursor: pointer;
        display: inline-block;
        height: $size;
        margin: 0 $size/3;
        position: relative;
        width: $size;

        &--play {
            overflow: hidden;

            .rectangle,
            .triangle {
                height: $size;
                left: 0;
                position: absolute;
                top: 0;
                width: $size;
            }
            // .rectangle, .triangle

            .rectangle {
                z-index: 5;

                &:before,
                &:after {
                    @include transition(all $speed ease);
                    background-color: $color-yellow;
                    content: '';
                    height: 100%;
                    width: 50%;

                    .player--playing & {
                        width: 36%;
                    }
                    // .player--playing & 

                }
                // &:before, &:after

                &:before {
                    float: left;
                    overflow :hidden;
                }
                // &:before

                &:after {
                    float: right;
                }
                // &:before

            }
            // .rectangle 

            .triangle {
                z-index: 10;

                &:before,
                &:after {
                    @include transition(all $speed ease);
                    background-color: transparent;
                    border-bottom: $size/2 solid transparent;
                    border-right: $size solid #fff;
                    border-top: $size/2 solid transparent;
                    content: '';
                    height: 0;
                    position: absolute;
                    right: 0;
                    top: 0;
                    width: 0;
                }
                // &:before, &:after

                &:before {
                    @include transform(translate(0, -50%));

                    .player--playing & {
                        @include transform(translate(0, -100%));
                    }
                    // .player--playing & 

                }
                // &:before

                &:after {
                    @include transform(translate(0, 50%));

                    .player--playing & {
                        @include transform(translate(0, 100%));
                    }
                    // .player--playing & 

                }
                // &:after

            }
            // .triangle

            &:hover {

                .rectangle {

                    &:before,
                    &:after {
                        background-color: darken($color-yellow, 10%);
                    }
                    // &:before, &:after

                }
                // .rectangle 

            }
            // &:hover 

        }
        // &--play

        &--next,
        &--prev {
            width: 45px;

            &:before,
            &:after {
                @include transition(all $speed ease);
                border-bottom: $size/2 solid transparent;
                border-top: $size/2 solid transparent;
                content: '';
                height: 0; 
                position: absolute;
                top: 0;
                width: 0; 
            }
            // &:before, &:after

        }
        // &--next, &--prev

        &--next {
            width: 45px;
            
            &:before,
            &:after {
                border-left: $size solid $color-yellow;
            }
            // &:before, &:after

            &:before {
                left: 0;
            }
            // &:before

            &:after {
                left: $size/1.5;
            }
            // &:before

            &:hover {

                &:before,
                &:after {
                   border-left-color: darken($color-yellow, 10%);
                }
                // &:before, &:after

            }
            // &:hover

        }
        // &--next

        &--prev {  

            &:before,
            &:after {
                border-right: $size solid $color-yellow;
            }
            // &:before, &:after

            &:before {
                right: 0;
            }
            // &:before

            &:after {
                right: $size/1.5;
            }
            // &:before

            &:hover {

                &:before,
                &:after {
                   border-right-color: darken($color-yellow, 10%);
                }
                // &:before, &:after

            }
            // &:hover

        }
        // &--prev

    }
    // &-item

}
// .player__controls

.album {
    @include transform(translateY(-50%));
    @include transition(all $transition-time $transition-method);
    box-shadow: 0px 0px 10px 0px rgba($color-black, 0.4);
    cursor: pointer;
    height: $album-size;
    position: absolute;
    right: 0;
    top: 50%;
    width: $album-size;
    z-index: 100;

    .player--open & {
        cursor: default;
        right: -100px;
    }
    // .player--open & 

    &__cover {
        background-color: $color-black;
        background-size: cover;
        height: 100%;
        position: relative;
        width: 100%;
        z-index: 20;
    }
    // &__cover 

    &:hover {

        .vinyl {
            left: 25%;
        }
        // .vinyl 

    }
    // &:hover

}
// .album

.album--billionaires-2014-compilation {

    .album__cover,
    .vinyl .vinyl__center:before {
        background-image: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/43525/album-billionaires-2014-compilation.jpg');
    }
    // .album__cover, .vinyl .vinyl__center:before 

}
// .album--billionaires-2014-compilation 

.album--project-mayhem {

    .album__cover,
    .vinyl .vinyl__center:before {
        background-image: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/43525/album-project-mayhem.jpg');
    }
    // .album__cover, .vinyl .vinyl__center:before 

}
// .album--project-mayhem 

.album--boxer {

    .album__cover,
    .vinyl .vinyl__center:before {
        background-image: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/43525/album-boxer.jpg');
    }
    // .album__cover, .vinyl .vinyl__center:before 

}
// .album--boxer 

.vinyl {
    @include transition(all $transition-time $transition-method);
    left: $vinyl-offset/2;
    position: absolute;
    top: $vinyl-offset/2;
    height: $vinyl-size;
    width: $vinyl-size;
  
    .player--open & {
        left: 0 !important;
    }
    // .player--open & 
  
    .player--playing & {
        left: 50% !important;
    }
    // .player--playing & 

    &__shadow,
    &__circle {
        border-radius: 100%;
        height: 100%;
        left: 0;
        position: absolute;
        top: 0;
        width: 100%;
    }
    // &__shadow, &__circle

    &__shadow {
        box-shadow: 2px 8px 10px 0 rgba($color-black, 0.15);
        z-index: 5;       
    }
    // &__shadow 

    &__circle {
        @include animation(rotate 1.0s linear infinite both paused);
        background-color: #262121;
        z-index: 10;

        .player--playing & {
            @include animation-play-state(running);
        }
        // .player--playing & 

    }
    // &__circle 

    &__center {
        @include transform(translate(-50%, -50%));
        background-color: #292424;
        border-radius: 100%;
        height: $vinyl-center-size;
        left: 50%;
        position: absolute;
        top: 50%;
        width: $vinyl-center-size;

        &:before,
        &:after {
            @include transform(translate(-50%, -50%));
            border-radius: 100%;
            content: '';
            left: 50%;
            position: absolute;
            top: 50%;
        }

        &:before {
            background-color: #ed7167;
            background-size: cover;
            height: 116px;
            width: 116px;
            z-index: 5;
        }
        // &:before

        &:after {
            background-color: #fff;
            height: 40px;
            width: 40px;
            z-index: 10;
        }
        // &:after

    }
    // &__center

}
// .vinyl

////
// Helpers
////

.has-fade-in {
    @include transition(all $transition-time*2 $transition-method);
    opacity: 0;

    .player--open & {
        opacity: 1;
    }
    // .player--open &

}
// .has-fade-in

////
// Keyframes
////

@include keyframes(rotate) {

    from {
        @include transform(rotate(0deg));
    }

    to {
        @include transform(rotate(360deg));
    }

}
// @include keyframes(rotate) 

JAVASCRIPT-FILE
// Player
var Player = function() {
    var _this = this,
    $playerAll = $('[data-player]'),
    $playerCurrent = null,
    $displayArtistName = null,
    $displayAlbumName = null,
    $displaySongName = null,
    $controlPrev = $('[data-player-prev]'),
    $controlPlay = $('[data-player-play]'),
    $controlNext = $('[data-player-next]'),
    index = 0,
    path = {
        audio: 'http://lab.islegend.com/challenge/music-player/assets/audio/'
    },
    playing = false,
    playlist = null,
    audio = null;

    _this.methods = {
        init: function() {
            _this.methods.bindUserEvents();
        },
        bindUserEvents: function() {

            $playerAll.on('click', function() {

                if ( !$(this).hasClass('player--open') ) {

                    // pause the current player
                    if (audio !== null) { 
                        audio.pause(); 
                        $playerCurrent.removeClass('player--open player--playing');
                    }

                    // get new player
                    $playerCurrent = $(this);
                    index = $playerCurrent.data('track');

                    // retrieve display elements
                    $displayArtistName = $playerCurrent.find('[data-player-album-artist]');
                    $displayAlbumName = $playerCurrent.find('[data-player-album-name]'),
                    $displaySongName = $playerCurrent.find('[data-player-album-song]');

                    // Audio
                    playlist = playlists[$playerCurrent.data('playlist')];
                    audio = $playerCurrent.find('audio').get(0);
                    audio.addEventListener('ended', function() { 
                        _this.methods.nextTrack();
                    });
                    if (!audio.src) { _this.methods.loadTrack(0); }
                    _this.methods.playTrack();

                    $playerCurrent.toggleClass('player--open');

                }

            });

            $controlPlay.on('click', function() {

                if ($playerCurrent.hasClass('player--playing')) {
                    _this.methods.pauseTrack();
                } else {
                    _this.methods.playTrack();
                }

            }); 

            $controlNext.on('click', function() {
                _this.methods.nextTrack();
            }); 

            $controlPrev.on('click', function() {
                _this.methods.prevTrack();
            }); 

        },
        loadTrack: function() {
            audio.src = path.audio + playlist.slug + '/' + playlist.tracks[index].file;
            $displayArtistName.text(playlist.tracks[index].artist);
            $displayAlbumName.text(playlist.tracks[index].album);
            $displaySongName.text(playlist.tracks[index].song);
            $playerCurrent.data('track', index);
        },
        playTrack: function() {
            $playerCurrent.addClass('player--playing');
            playing = true;
            audio.play();
        },
        pauseTrack: function() {
            $playerCurrent.removeClass('player--playing');
            playing = false;
            audio.pause();
        },
        nextTrack: function() {

            if ((index + 1) < playlist.trackCount) {
                index++;
            } else {
                index = 0;
            }

            _this.methods.loadTrack(index);

            if (playing) {
                audio.play();
            }

        },
        prevTrack: function() {

            if ((index - 1) > -1) {
                index--;
            } else {
                index = (playlist.trackCount - 1);
            }

            _this.methods.loadTrack(index);

            if (playing) {
                audio.play();
            }

        }
    };

    return _this.methods;

};

// Load
$(function() {
    player = new Player();
    player.init();
});

// Data
var playlists = {
    billionaires2014Compilation: {
        slug: "billionaires-2014-compilation",
        trackCount: 17,
        tracks: [
            {
                "track": 1,
                "artist": "Another Monster",
                "album": "Press Play EP",
                "song": "Drop It Low",
                "file": "another-monster-drop-it-low.mp3"
            }, {
                "track": 2,
                "artist": "George Antonios",
                "album": "Billionaires 2014 Compilation",
                "song": "Signals In The Dark",
                "file": "george-antonios-signals-in-the-dark.mp3"
            }, {
                "track": 3,
                "artist": "Hypercube",
                "album": "Billionaires 2014 Compilation",
                "song": "Analog Circuits",
                "file": "hypercube-analog-circuits.mp3"
            }, {
                "track": 4,
                "artist": "Klarity",
                "album": "Truth & Lies EP",
                "song": "Second Nature",
                "file": "klarity-second-nature.mp3"
            }, {
                "track": 5,
                "artist": "Clerks",
                "album": "Zone 6 Wizard EP",
                "song": "Drama",
                "file": "clerks-drama.mp3"
            }, {
                "track": 6,
                "artist": "M00DY",
                "album": "Super Squad EP",
                "song": "Voyage",
                "file": "m00dy-voyage.mp3"
            }, {
                "track": 7,
                "artist": "Shuhandz",
                "album": "Get Weird Remix EP",
                "song": "Get Weird",
                "file": "shuhandz-get-weird.mp3"
            }, {
                "track": 8,
                "artist": "Bad Catholics",
                "album": "Super Squad EP",
                "song": "Astapor",
                "file": "bad-catholics-astapor.mp3"
            }, {
                "track": 9,
                "artist": "Aaron Sigmon",
                "album": "Pop Dat Booty EP",
                "song": "Booty Bump (Trap Mix)",
                "file": "aaron-sigmon-booty-bump.mp3"
            }, {
                "track": 10,
                "artist": "Dope Arcade",
                "album": "Dead Wrong EP",
                "song": "HAL 9k",
                "file": "dope-arcade-hal-9k.mp3"
            }, {
                "track": 11,
                "artist": "Jason Wiggz",
                "album": "Super Squad EP",
                "song": "MegaTons",
                "file": "jason-wiggz-megatons.mp3"
            }, {
                "track": 12,
                "artist": "Kit Walters & Boy Beats World",
                "album": "Super Squad EP",
                "song": "New Mutiny",
                "file": "kit-walters-and-boy-beats-world-new-mutiny.mp3"
            }, {
                "track": 13,
                "artist": "Two Face",
                "album": "Super Squad EP",
                "song": "Diavolo",
                "file": "two-face-diavolo.mp3"
            }, {
                "track": 14,
                "artist": "Kyle Biddy",
                "album": "Super Squad EP",
                "song": "T2",
                "file": "kyle-biddy-t2.mp3"
            }, {
                "track": 15,
                "artist": "Vorheez",
                "album": "Spooked Out EP",
                "song": "Showtime",
                "file": "vorheez-showtime.mp3"
            }, {
                "track": 16,
                "artist": "Vorheez",
                "album": "Spooked Out EP",
                "song": "Spooked Out",
                "file": "vorheez-spooked-out.mp3"
            }, {
                "track": 17,
                "artist": "Patrick Bandy",
                "album": "A Day in the Life EP",
                "song": "Sakura (Samurai Sword)",
                "file": "patrick-bandy-sakura-samurai-sword.mp3"
            }
            
        ]
    },
    projectMayhem:  {
        slug: "project-mayhem",
        trackCount: 2,
        tracks: [
            {
                "track": 1,
                "artist": "Kyle Thatcher",
                "album": "Project: Mayhem",
                "song": "Commence",
                "file": "commence.mp3"
            }, {
                "track": 2,
                "artist": "Kyle Thatcher",
                "album": "Project: Mayhem",
                "song": "Bouncy Green Slime",
                "file": "bouncy-green-slime.mp3"
            }
        ]
    },
    boxer:  {
        slug: 'boxer',
        trackCount: 2,
        tracks: [
            {
                "track": 1,
                "artist": "The National",
                "album": "Boxer",
                "song": "Fake Empire",
                "file": "fake-empire.mp3"
            }, {
                "track": 1,
                "artist": "The National",
                "album": "Boxer",
                "song": "Mistaken For Strangers",
                "file": "mistaken-for-strangers.mp3"
            }
        ]
    }
}
